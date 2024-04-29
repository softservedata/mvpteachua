# TeachUA project (Frontend and Backend)

## Project Overview

This project is a web application that allows users to search for children's clubs with the Ukrainian language of instruction.

Here is two part:<br>
In folder `frontend` is front-end<br>
In folder `backend` is back-end<br>

### Key Features

1. **Authentication and Registration:** Users can create an account.

2. **Search Clubs:** Users can search for clubs in different cities.

---

## DATABASE

> Before you begin, make sure your MariaDB/MySQL database contains a database with a name like 'teachua'.

- You can create a database using a command
```sql
create database teachua2 character set utf8 collate utf8_bin;
```
- The ```./data.sql``` file contains a script for creating tables and populating initial data.

---

## BACK-END

### Technical Details

- **Back-end programming language:** Java
- **Database:** MariaDB/MySQL
- **Required Tools:** Java 17, Maven 3.6.3

### **Database Configuration**

In the application's configuration file
```text
./backend/src/main/resources/application.properties
```
the path and database connection details are obtained from the following environment variables:

- JDBC_DRIVER - the full name of the database connection driver; for example
```text
org.mariadb.jdbc.Driver
com.mysql.cj.jdbc.Driver
```
- DATASOURCE_URL - connection string to the database; for example
```text
jdbc:mariadb://127.0.0.1:3306/teachua
jdbc:mysql://127.0.0.1:3306/teachua?useUnicode=true&serverTimezone=UTC
```
- DATASOURCE_USER - user name;
- DATASOURCE_PASSWORD - user password;

Before starting, make sure that the MariaDB/MySQL database contains an empty database.

### Running the Project

1. **Go to folder backend:**
```bash
cd backend
```

2. **Build the Project:**

Execute the following command in the `backend` directory:
```bash
mvn clean package
```

3. **Run the Project:**

After successful building, run the .jar file in the ./target folder:
```bash
java -jar target/dev.war
```
```text
The application will start on 8080 port.
```

---

## FRONT-END

### Technical Details

- **Front-end written on:** React JS;
- **Required Tools:** nodejs 16 version.

### Running the Project

1. **Go to folder frontend:**
```bash
cd frontend
```
2. **Download Dependencies:**

   Execute the following command in the `frontend` directory:
```bash
npm install
```

3. **Write the path to the backend server** into the REACT_APP_ROOT_SERVER environment variable for example
```text
http://localhost:8080
```

4. **Run the Project:**

After successful building you could run the front-end in dev mode:

```bash
npm run start
```
```text
The application will start on 3000 port.
```

To build the front-end to production run command:

```bash
npm run build
```
```text
    The application will appear in the ./build folder.
    Copy all files in your webserver and configure it.
```

Notes

The project is at an early stage of development, currently only club search is implemented.

---

> Press CTRL+C to stop applications.

We wish you success in the "TeachUA" project!

---
