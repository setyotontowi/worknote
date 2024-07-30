---
tags: [Research]
title: Express 101
created: '2024-07-18T08:08:09.525Z'
modified: '2024-07-18T08:08:20.221Z'
---

# Express 101

To set up a clean and organized Express.js project with Sequelize, you can follow a structured file directory. Here is an example of how you can organize your project:

```
my-express-app/
├── config/
│   └── database.js
├── controllers/
│   └── cityController.js
│   └── patientController.js
├── models/
│   └── index.js
│   └── city.js
│   └── patient.js
├── routes/
│   └── index.js
│   └── cityRoutes.js
│   └── patientRoutes.js
├── app.js
├── package.json
└── .env
```

### 1. `config/database.js`

This file will set up and configure the Sequelize instance.

```javascript
const { Sequelize } = require('sequelize');

const sequelize = new Sequelize(process.env.DB_NAME, process.env.DB_USER, process.env.DB_PASS, {
    host: process.env.DB_HOST,
    dialect: 'mysql'
});

module.exports = sequelize;
```

### 2. `models/index.js`

This file will initialize your models and define any associations.

```javascript
const Sequelize = require('sequelize');
const sequelize = require('../config/database');

const City = require('./city')(sequelize, Sequelize);
const Patient = require('./patient')(sequelize, Sequelize);

// Define associations
City.hasMany(Patient, { foreignKey: 'city_id' });
Patient.belongsTo(City, { foreignKey: 'city_id' });

module.exports = {
    City,
    Patient,
    sequelize
};
```

### 3. `models/city.js`

This file defines the City model.

```javascript
module.exports = (sequelize, DataTypes) => {
    const City = sequelize.define('City', {
        city_id: {
            type: DataTypes.INTEGER,
            primaryKey: true,
            autoIncrement: true
        },
        city_name: {
            type: DataTypes.STRING,
            allowNull: false
        }
    }, {
        tableName: 'cities',
        timestamps: false
    });
    return City;
};
```

### 4. `models/patient.js`

This file defines the Patient model.

```javascript
module.exports = (sequelize, DataTypes) => {
    const Patient = sequelize.define('Patient', {
        patient_id: {
            type: DataTypes.INTEGER,
            primaryKey: true,
            autoIncrement: true
        },
        city_id: {
            type: DataTypes.INTEGER,
            allowNull: false
        }
    }, {
        tableName: 'patients',
        timestamps: false
    });
    return Patient;
};
```

### 5. `controllers/cityController.js`

This file contains the controller logic for cities.

```javascript
const { City, Patient, sequelize } = require('../models');

const getCityPatientCounts = async (req, res) => {
    try {
        const result = await City.findAll({
            include: {
                model: Patient,
                attributes: []
            },
            attributes: [
                'city_name',
                [sequelize.fn('COUNT', sequelize.col('Patients.patient_id')), 'patient_count']
            ],
            group: ['City.city_id', 'City.city_name'],
            order: [[sequelize.literal('patient_count'), 'DESC']]
        });
        res.json(result);
    } catch (error) {
        res.status(500).json({ error: error.message });
    }
};

module.exports = {
    getCityPatientCounts
};
```

### 6. `routes/index.js`

This file sets up the main routes for the application.

```javascript
const express = require('express');
const router = express.Router();

const cityRoutes = require('./cityRoutes');
const patientRoutes = require('./patientRoutes');

router.use('/cities', cityRoutes);
router.use('/patients', patientRoutes);

module.exports = router;
```

### 7. `routes/cityRoutes.js`

This file sets up the routes for city-related endpoints.

```javascript
const express = require('express');
const router = express.Router();
const cityController = require('../controllers/cityController');

router.get('/patient-counts', cityController.getCityPatientCounts);

module.exports = router;
```

### 8. `routes/patientRoutes.js`

You can define patient-related routes here if needed.

```javascript
const express = require('express');
const router = express.Router();

// Define patient-related routes here

module.exports = router;
```

### 9. `app.js`

This file initializes the Express app and sets up middleware.

```javascript
require('dotenv').config();
const express = require('express');
const app = express();
const routes = require('./routes');
const { sequelize } = require('./models');

// Middleware
app.use(express.json());
app.use('/api', routes);

// Sync database and start the server
const PORT = process.env.PORT || 3000;

sequelize.sync()
    .then(() => {
        app.listen(PORT, () => {
            console.log(`Server is running on port ${PORT}`);
        });
    })
    .catch(error => {
        console.error('Unable to connect to the database:', error);
    });
```

### 10. `.env`

Store your database credentials here.

```
DB_NAME=your_database_name
DB_USER=your_database_user
DB_PASS=your_database_password
DB_HOST=your_database_host
PORT=3000
```

### 11. `package.json`

Make sure you have the necessary dependencies in your `package.json`.

```json
{
  "name": "my-express-app",
  "version": "1.0.0",
  "description": "A clean code Express.js application with Sequelize",
  "main": "app.js",
  "scripts": {
    "start": "node app.js"
  },
  "dependencies": {
    "dotenv": "^10.0.0",
    "express": "^4.17.1",
    "mysql2": "^2.2.5",
    "sequelize": "^6.6.5"
  }
}
```

With this setup, you have a clean and organized structure for your Express.js project, making it easier to manage and maintain as it grows.
