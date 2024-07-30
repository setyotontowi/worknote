---
tags: ['2024/[07] July']
title: Multiple Java Version
created: '2024-07-30T01:19:00.049Z'
modified: '2024-07-30T01:19:09.512Z'
---

# Multiple Java Version

To install multiple Java versions on Ubuntu and switch between them, you can follow these steps:

### 1. **Download and Install Java Versions**

You can install different Java versions from the Ubuntu repository or download them from the Oracle website.

#### **From the Repository:**
```bash
sudo apt update
# Install Java 8
sudo apt install openjdk-8-jdk
# Install Java 11
sudo apt install openjdk-11-jdk
# Install Java 17
sudo apt install openjdk-17-jdk
```

#### **From Oracle Website:**
1. Download the desired version from the [Oracle Java website](https://www.oracle.com/java/technologies/javase-downloads.html).
2. Extract the downloaded archive to a directory (e.g., `/usr/lib/jvm/`):
   ```bash
   sudo mkdir -p /usr/lib/jvm
   sudo tar -xvf jdk-<version>-linux-x64.tar.gz -C /usr/lib/jvm/
   ```

### 2. **Set Up Java Alternatives**

Use the `update-alternatives` command to manage different Java versions.

```bash
sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/<java_version>/bin/java 1
sudo update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/<java_version>/bin/javac 1
```

Replace `<java_version>` with the specific path of the Java version you installed. The number at the end represents the priority; a higher number means higher priority.

### 3. **Switch Between Java Versions**

To switch between the installed Java versions, use the `update-alternatives` command:

```bash
sudo update-alternatives --config java
```

You'll see a list of installed Java versions. Enter the number corresponding to the version you want to use and press Enter.

You can do the same for `javac`:

```bash
sudo update-alternatives --config javac
```

### 4. **Set JAVA_HOME Environment Variable**

To set the `JAVA_HOME` environment variable, you can add it to your shell configuration file (`.bashrc`, `.zshrc`, etc.):

1. Open the file in a text editor:
   ```bash
   nano ~/.bashrc
   ```
2. Add the following line at the end of the file, replacing `<java_version>` with your desired Java version path:
   ```bash
   export JAVA_HOME=/usr/lib/jvm/<java_version>
   export PATH=$JAVA_HOME/bin:$PATH
   ```
3. Save and close the file.

4. Apply the changes:
   ```bash
   source ~/.bashrc
   ```

This setup allows you to install, configure, and switch between multiple Java versions on Ubuntu.
