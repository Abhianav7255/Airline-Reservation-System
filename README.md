# Airline Reservation System

This project is a simple Airline Reservation System implemented in C++ using MySQL for database management. The system allows users to:

- Insert flight details into the database.
- Reserve seats on specific flights.

## Features
- **Database Connection**: Establishes a connection to a MySQL database to store and manage flight information.
- **Flight Management**: Adds flight details such as flight number, departure, destination, and available seats.
- **Seat Reservation**: Updates seat availability when a user reserves a seat on a specific flight.

---

## Prerequisites

1. **MySQL**: Ensure you have MySQL installed and a database created with the required schema.
2. **C++ Compiler**: A compiler like `g++` that supports C++11 or later.
3. **Libraries**:
   - MySQL Connector C++
   - Windows-specific headers like `<windows.h>`

---

## Database Setup

### Create Database and Table
Run the following SQL commands to set up the required database and table:

```sql
CREATE DATABASE mydb;
USE mydb;

CREATE TABLE Airline (
    Fnumber VARCHAR(50),
    Departure VARCHAR(50),
    Destination VARCHAR(50),
    Seat INT
);
```

### Configure Database Credentials
Modify the constants in the source code to match your MySQL setup:

```cpp
const char* HOST = "localhost";
const char* USER = "root";
const char* PW = "your password";
const char* DB = "mydb";
```

---

## Installation and Compilation

### Install MySQL Connector
- Download and install the MySQL Connector for C++.
- Link the MySQL libraries during compilation.

### Compilation
Compile the code using a C++ compiler like `g++`:

```bash
g++ -o airline_reservation airline_reservation.cpp -lmysqlcppconn
```

---

## Usage

1. Run the compiled program:
   ```bash
   ./airline_reservation
   ```

2. Follow the on-screen instructions to:
   - View a welcome message.
   - Reserve a seat on a flight.
   - Exit the application.

---

## Known Issues

- **Code Bugs**:
  - Unmatched variable names: Ensure consistency between variable names in the `Flight` class and methods.
  - Missing headers and syntax errors (e.g., `unistd.h` for `sleep`, `stringstream` not correctly handling integers).
  - Logical errors in SQL queries and variable concatenations.
- **Error Handling**: Improve error handling for database queries and incorrect user inputs.
- **Windows Compatibility**: Use `Sleep()` instead of `sleep()` on Windows systems.

---

## Contributions

Contributions are welcome! Please fork the repository and create a pull request for any enhancements or bug fixes.

---

## License

This project is licensed under the MIT License. Feel free to use and modify it as needed.

---

## Acknowledgments

Special thanks to the developers of MySQL and the C++ language for making such projects possible!
