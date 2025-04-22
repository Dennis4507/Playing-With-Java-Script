# JavaScript Skeleton Project

This project demonstrates a basic HTML structure with embedded JavaScript to explore variable declarations, reassignments, and constants in JavaScript. Below is a detailed explanation of the code and the steps taken during the development process.

---

## Project Structure

The main file in this project is `index.html`, which contains the following:

1. **HTML Structure**:
   - A `<meta>` tag for responsive design.
   - A `<title>` tag for the page title.
   - A `<body>` section with an `<h1>` heading and a `<script>` tag for JavaScript.

2. **JavaScript Code**:
   - Demonstrates variable declarations using `let` and `const`.
   - Explains reassignment rules for variables and constants.
   - Outputs variable values to the browser console.

---

## Key Code and Comments

### HTML Structure
    <script>
        let name = "John";
        let surname = "Doe";
        let age = 11;
        age = 54; // Reassigning the value of `age`
        let isStudent = true;

        // Notice the lack of `let` on line 14 - we don’t need it since the variable has already been declared earlier and we are just re-assigning it here
    </script>
Key Learning Points
Variable Declaration:

Use let for variables that may change.
Use const for variables that should remain constant.
Reassignment Rules:

Variables declared with let can be reassigned.
Constants declared with const cannot be reassigned.
Debugging:

Use console.log() to output variable values and debug your code.


Fixing Errors
Original Issue
The code attempted to reassign the constant pi, which caused a runtime error:

// pi = 10; // This will throw an error because `pi` is a constant and cannot be reassigned

Solution
To fix the error, the reassignment was removed:
const pi = 3.14;
// Removed the line: pi = 10;