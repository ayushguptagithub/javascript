

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript Basics</title>
</head>
<body>
    <section id="main-section">
        <h1>JavaScript Basics Examples</h1>
        <button id="eventButton">Click Me</button>
        <p id="output"></p>
    </section>

    <script>
        // 1. Data Types
        console.log("---- Data Types ----");
        let number = 42; // Number
        let string = "Hello, World!"; // String
        let boolean = true; // Boolean
        let undefinedValue; // Undefined
        let nullValue = null; // Null
        console.log(typeof number, typeof string, typeof boolean, typeof undefinedValue, typeof nullValue);

        // 2. Variables
        console.log("---- Variables ----");
        var oldVar = "Var keyword (not recommended)";
        let newVar = "Let keyword (block scoped)";
        const constantVar = "Const keyword (constant)";
        console.log(oldVar, newVar, constantVar);

        // 3. Types of Prompts and Printing
        console.log("---- Prompts and Printing ----");
        // Uncomment to test prompts
        // let name = prompt("What's your name?");
        // let age = confirm("Are you above 18?");
        // console.log(`Name: ${name}, Above 18: ${age}`);

        // 4. If-Else and Else-If Conditions
        console.log("---- If-Else and Else-If ----");
        let marks = 85;
        if (marks >= 90) {
            console.log("Grade: A");
        } else if (marks >= 75) {
            console.log("Grade: B");
        } else {
            console.log("Grade: C");
        }

        // 5. Conditional (Ternary) Operator
        console.log("---- Conditional Operator ----");
        let isPass = marks >= 40 ? "Pass" : "Fail";
        console.log(`Result: ${isPass}`);

        // 6. Loops
        console.log("---- Loops ----");
        console.log("For Loop:");
        for (let i = 1; i <= 5; i++) {
            console.log(`Iteration ${i}`);
        }

        console.log("While Loop:");
        let counter = 1;
        while (counter <= 5) {
            console.log(`Iteration ${counter}`);
            counter++;
        }

        console.log("Do-While Loop:");
        let count = 1;
        do {
            console.log(`Iteration ${count}`);
            count++;
        } while (count <= 5);

        // 7. Element Selectors
        console.log("---- Element Selectors ----");
        const section = document.getElementById('main-section'); // By ID
        const button = document.querySelector('button'); // By Query Selector
        const paragraphs = document.getElementsByTagName('p'); // By Tag Name
        console.log(section, button, paragraphs);

        // 8. Functions
        console.log("---- Functions ----");
        // Function Declaration
        function add(a, b) {
            return a + b;
        }
        console.log(`Addition: ${add(5, 10)}`);

        // Arrow Function
        const multiply = (a, b) => a * b;
        console.log(`Multiplication: ${multiply(5, 10)}`);

        // 9. Events
        console.log("---- Events ----");
        button.addEventListener('click', function () {
            document.getElementById('output').textContent = "Button was clicked!";
            console.log("Button clicked event handled.");
        });
    </script>
</body>
</html>
```

### Topics Covered:
1. **Data Types**:
   - Includes `number`, `string`, `boolean`, `undefined`, and `null`.

2. **Variables**:
   - Usage of `var`, `let`, and `const`.

3. **Prompts and Printing**:
   - Examples of `prompt()`, `confirm()`, and `console.log()`.

4. **Conditions**:
   - `if`, `else if`, `else`, and the conditional (ternary) operator.

5. **Loops**:
   - `for`, `while`, and `do-while` loops.

6. **Element Selectors**:
   - Using `getElementById`, `querySelector`, and `getElementsByTagName`.

7. **Functions**:
   - Demonstrates function declarations and arrow functions.

8. **Events**:
   - Event listener for a button click.

This code provides an overview of basic JavaScript concepts with practical examples for each. You can test it in a browser, and interact with the button to see how events are handled.