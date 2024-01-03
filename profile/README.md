# FRS - FRecipe System

## Table of Contents
- [Installation](#installation)

## Installation

### Setup maven environment 
- Download and install maven from [here](https://maven.apache.org/download.cgi)
- Add maven to your path
- Check if maven is installed correctly by running `mvn -v` in your terminal
- Create a new file called `settings.xml` in folder (e.g. `C:\Users\{username}\.m2\`) and paste the following code into it:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
          xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 http://maven.apache.org/xsd/settings-1.0.0.xsd">
    <activeProfiles>
        <activeProfile>github</activeProfile>
    </activeProfiles>

    <profiles>
        <profile>
            <id>github</id>
            <repositories>
                <repository>
                    <id>github</id>
                    <url>https://maven.pkg.github.com/G2-SE1717-JS/frs-platform</url>
                    <snapshots>
                        <enabled>true</enabled>
                    </snapshots>
                </repository>
            </repositories>
        </profile>
    </profiles>


    <servers>
        <server>
            <id>github</id>
            <username>${username_github}</username>
            <password>${password_github}</password>
        </server>
    </servers>
</settings>
```

### Clone repositories

- Clone the following repositories:
  - [FRS-Platform](https://github.com/G2-SE1717-JS/frs-platform)
  - [FRS-Core](https://github.com/G2-SE1717-JS/frs-core)
  - [FRS-Application](https://github.com/G2-SE1717-JS/frs-application)

### Note
- The following steps are required for each repository
- Replace `{username}` with your github username
- Replace `{password}` with your github password
- Replace `{path}` with the path to the repository
- If you are development Api only need to clone `FRS-Application` (follow the steps below)
