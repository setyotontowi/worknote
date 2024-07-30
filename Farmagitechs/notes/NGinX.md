---
tags: ['2024/[07] July']
title: NGinX
created: '2024-07-29T04:37:41.031Z'
modified: '2024-07-29T04:37:58.503Z'
---

# NGinX

To set up a local web development environment similar to XAMPP but using Nginx, PHP, and MySQL (also known as the LEMP stack), follow these steps:

### 1. Install Nginx, PHP, and MySQL

On a Debian-based system (like Ubuntu), use the following commands to install Nginx, PHP, and MySQL:

```bash
sudo apt update
sudo apt install nginx php-fpm php-mysql mysql-server
```

On a Red Hat-based system (like CentOS), use:

```bash
sudo yum install epel-release
sudo yum install nginx php-fpm php-mysqlnd mariadb-server
```

### 2. Start and Enable Services

Ensure that Nginx, PHP-FPM, and MySQL services are started and enabled to start on boot:

```bash
sudo systemctl start nginx
sudo systemctl enable nginx

sudo systemctl start php-fpm
sudo systemctl enable php-fpm

sudo systemctl start mysql
sudo systemctl enable mysql
```

### 3. Secure MySQL Installation

Run the following command to secure your MySQL installation:

```bash
sudo mysql_secure_installation
```

Follow the prompts to set a root password and secure your MySQL server.

### 4. Configure Nginx to Use PHP-FPM

Create a new server block configuration for your site. For example, create a file named `lemp.conf` in `/etc/nginx/sites-available/`:

```bash
sudo nano /etc/nginx/sites-available/lemp.conf
```

Add the following configuration to the file:

```nginx
server {
    listen 80;
    server_name localhost;
    
    root /var/www/html;
    index index.php index.html index.htm;

    location / {
        try_files $uri $uri/ =404;
    }

    location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/var/run/php/php7.4-fpm.sock; # Adjust PHP version if necessary
        fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
        include fastcgi_params;
    }

    location ~ /\.ht {
        deny all;
    }
}
```

Enable the new configuration by creating a symbolic link in the `sites-enabled` directory:

```bash
sudo ln -s /etc/nginx/sites-available/lemp.conf /etc/nginx/sites-enabled/
```

Remove the default server block if it exists:

```bash
sudo rm /etc/nginx/sites-enabled/default
```

### 5. Test Nginx Configuration and Restart

Test the Nginx configuration for syntax errors:

```bash
sudo nginx -t
```

If the test is successful, restart Nginx to apply the changes:

```bash
sudo systemctl restart nginx
```

### 6. Create a PHP Test File

Create a simple PHP file to test your setup. Place this file in your web root directory:

```bash
echo "<?php phpinfo(); ?>" | sudo tee /var/www/html/index.php
```

### 7. Adjust Permissions

Ensure the web root directory has the correct permissions:

```bash
sudo chown -R www-data:www-data /var/www/html
sudo chmod -R 755 /var/www/html
```

### 8. Access Your Local Site

Open a web browser and navigate to `http://localhost`. You should see the PHP information page, confirming that your LEMP stack is working correctly.

### 9. Installing phpMyAdmin (Optional)

If you need a web-based interface to manage your MySQL databases, you can install phpMyAdmin:

```bash
sudo apt install phpmyadmin
```

When prompted, select Nginx as the web server (or configure manually if not prompted).

### 10. Configuring phpMyAdmin with Nginx

Create a new Nginx server block or add the configuration to an existing one to serve phpMyAdmin:

```nginx
server {
    listen 80;
    server_name localhost;
    
    root /var/www/html;
    index index.php index.html index.htm;

    location / {
        try_files $uri $uri/ =404;
    }

    location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/var/run/php/php7.4-fpm.sock; # Adjust PHP version if necessary
        fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
        include fastcgi_params;
    }

    location ~ /\.ht {
        deny all;
    }

    location /phpmyadmin {
        root /usr/share/;
        index index.php index.html index.htm;
        location ~ ^/phpmyadmin/(.+\.php)$ {
            try_files $uri =404;
            root /usr/share/;
            fastcgi_pass unix:/var/run/php/php7.4-fpm.sock; # Adjust PHP version if necessary
            fastcgi_index index.php;
            fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
            include fastcgi_params;
        }
        location ~* ^/phpmyadmin/(.+\.(jpg|jpeg|gif|css|png|js|ico|html|xml|txt))$ {
            root /usr/share/;
        }
    }
}
```

Restart Nginx:

```bash
sudo systemctl restart nginx
```

You can now access phpMyAdmin at `http://localhost/phpmyadmin`.

With these steps, you should have a local web development environment similar to XAMPP, but using Nginx, PHP-FPM, and MySQL.
