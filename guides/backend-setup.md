# Backend Requirement

# Installer / Download

- Bruno
- Intellij
- maven
- Java JDK 17 (compatible for long term)
- postgresql
- dbeaver

# Repository

Clone from here - https://github.com/faizaldong/u4-wattsense-backend.git

# How to install / setup Java JDK 17 / Maven

Java JDK

- Get installer here - https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html
- move the folder to Program Files folder
- Windows -> search environment. In User variables for USER section,
  - Click new button, Variable name = JAVA_HOME, Variable value = path to jdk-x.x.
  - Select path and click edit, click new, add %JAVA_HOME%\bin

Maven

- Get installer here - https://maven.apache.org/download.cgi
- Choose Binary zip archive
- Exract the folder and move to Program Files folder
- Windows -> search environment. In User variables for USER section,
  - Click new button, Variable name = MAVEN_HOME, Variable value = path to apache-maven-x.x.
  - Select path and click edit, click new, add %MAVEN_HOME%\bin

Once both added to the User environment variables, restart the terminal and run
echo $MAVEN_HOME / $JAVA_HOME, you should see the path of the installer folder

# Intellij

## For new Project

On top left, click the New Project option. In popup, on left list, click on Spring Boot.

- Location - choose where to save your project
- Language - Java
- Type - Maven
- Group - com.[name-of-project]

## Add Environment variables

On top middle, make sure you see name of your project, if you didn't see it, please run the application first. Then, you will same your name project appear.

Click on the project name, from the list, select [Edit Configuration]. In the popup, fubd button [Modify options], then find Environment variables and select it. New field shown in the popup.

## What is use of resources folder?

- java folder -> logic
- resources -> configuration + data + static content

Normal files contained in this folder is application.yml / application.properties.
The file is used for

- database config(URL, username, password, etc)
- port server
- logging
- feature flags

Sample content of .yml file

```
spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/wattsense_db
    username: postgres
    password: ${DB_PASSWORD}

  jpa:
    hibernate:
      ddl-auto: update
    show-sql: true

  application:
    name: wattsense

  profiles:
    active: dev
```

If user Postgresql as a Database, have to install postgresql driver. Open `pm.xml` and add the dependency

``
  <dependency>
      <groupId>org.postgresql</groupId>
      <artifactId>postgresql</artifactId>
      <scope>runtime</scope>
  </dependency>
```


