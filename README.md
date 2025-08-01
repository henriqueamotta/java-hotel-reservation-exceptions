# Case Study: Exception Handling with Dates in Java

A simple Java project to demonstrate the application of custom exception handling in business rule validation involving dates, simulating a hotel reservation.

## 🎯 Project Objective

The main purpose of this repository is to serve as a practical example of how to manage and validate input data, specifically dates, using custom exceptions. The program reads reservation data, allows for updates, and ensures that business rules — such as not being able to schedule a check-out date before the check-in date and prohibiting updates to past reservations — are respected.

## ✨ Concepts Applied

-   **Object-Oriented Programming (OOP)**: Structuring the code into entities (`Reservation`) and the application layer.
-   **Date Handling**: Using the `LocalDate` and `DateTimeFormatter` classes to parse and calculate the duration between dates.
-   **Exception Handling**: Using `try-catch` blocks to gracefully control the application flow.
-   **Custom Exceptions**: Creating the `DomainException` class to represent errors specific to the hotel's business rules.

## ✔️ Business Rules Validated

1.  The check-out date must always be after the check-in date.
2.  Updates to a reservation can only be made for future dates. Past dates cannot be modified.

## ✔️ Repository Good Practices

This project follows good version control practices, using a `.gitignore` file to ensure that only the source code is committed to the repository. Compiled files (`.class`), packages (`.jar`, `.war`), logs, and IDE-specific files are correctly ignored, keeping the commit history clean and focused on what truly matters.

## 📂 Project Structure

```
src
├── application
│   └── Program.java         # Main class, responsible for user interaction and flow control.
└── model
    ├── entities
    │   └── Reservation.java # Entity class that represents the reservation and contains validation rules.
    └── exceptions
        └── DomainException.java # Custom exception for business domain errors.
```

## 🚀 How to Run

This is a plain Java project and requires no external dependencies other than the JDK.

1.  **Prerequisites:**
    * Have the [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/downloads/) installed (version 8 or higher).

2.  **Clone the repository:**
    ```bash
    git clone [https://github.com/henriqueamotta/exceptions001-java.git](https://github.com/henriqueamotta/exceptions001-java.git)
    ```

3.  **Compile the files:**
    ```bash
    javac -d bin src/application/Program.java src/model/entities/Reservation.java src/model/exceptions/DomainException.java
    ```

4.  **Run the application:**
    ```bash
    java -cp bin application.Program
    ```

The application will prompt for reservation data via the console and will validate inputs and updates according to the business rules.
