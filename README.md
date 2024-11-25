

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
        let pointNo = 1.2;
        document.write(number,string,boolean,pointNo);

        document.write("---------------------<br><br>");

        document.write(number,"<br>",string,"<br>",boolean,"<br>",pointNo,"<br>","<br>");

        document.write(typeof number,"<br>", typeof string,"<br>", typeof boolean,"<br>",typeof pointNo,"<br>");

        document.write(number," ",string," ",boolean," ",pointNo);

        // 2. Variables
        console.log("---- Variables ----");
        var oldVar = "Var keyword (not recommended)";
        var newVar = "var keyword (block scoped)";
        document.write(oldVar, newVar, constantVar);

        // 3. Types of Prompts and Printing
        console.log("---- Prompts and Printing ----");
        // Uncomment after trying
        var name = prompt("What's your name?");
        var age = confirm("Are you above 18?");
        alert(`Name: ${name}, Above 18: ${age}`);

        //Mathematical Concepts

        document.write("<br>Add two numbers : ",5+6);

        document.write("<br>Subtract two numbers : ",5-6);

        document.write("<br>Multiply two numbers : ",5*6);

        document.write("<br>Divide two numbers : ",5/6);

        document.write("<br>Square two numbers : ",Math.pow(3,2));

        document.write("<br>Square two numbers : ",5**2);

        document.write("<br>Square two numbers : ",Math.sqrt(25));


        **Question to solve in 5 min**
            - Take a user input of radius of circle and calculate Area of circle **hint(2 * pi* r)**
            - Take a user input i.e  Length and breadth ,Calcute the Area of Rectange **hint(l x b)**  
        
        

        // 4. If-Else and Else-If Conditions
        console.log("---- If-Else and Else-If ----");
        var marks = 85;
        if (marks >= 90) {
            console.log("Grade: A");
        } else if (marks >= 75) {
            console.log("Grade: B");
        } else {
            console.log("Grade: C");
        }

        // 5. Conditional (Ternary) Operator
        console.log("---- Conditional Operator ----");
        var isPass = marks >= 40 ? "Pass" : "Fail";
        console.log(`Result: ${isPass}`);

         **Question to solve in 10 min**
            - Take a user input i.e Age and if age is less then 18 display a message that "He is not eligible to vote" and if 18 or above display is "He is eligible" 
            - Program to Make A Simple Calculator.
 


        // 6. Loops
        console.log("---- Loops ----");
        console.log("For Loop:");
        for (var i = 1; i <= 5; i++) {
            document.write(`<br>Iteration `,i,"<br>");
        }

        console.log("While Loop:");
        var counter = 1;
        while (counter <= 5) {
            document.write(`Iteration ${counter}`);
            counter++;
        }

        console.log("Do-While Loop:");
        var count = 1;
        do {
            document.write(`Iteration ${count}`);
            count++;
        } while (count <= 5);

        // 7.Arrays

            var array = ['apple', 'banana', 'orange', 'Mango'];

            document.write(array,"<br>");

            var fruits=new Array("apple","mango");

            document.write(fruits,"<br>");

            document.write("Length of array : ",fruits.length);

            for (var i = 0; i < fruits.length; i++) { 
                document.write(fruits[i] , "</br>"); 
            }

            // 1. Accessing Elements
                document.write("First Element:", fruits[0]);
                document.write("Last Element:", fruits[fruits.length - 1]);

                // 2. Adding Elements
                fruits.push("Orange"); // Adds at the end
                document.write("After Push:", fruits);

                fruits.unshift("Mango"); // Adds at the beginning
                document.write("After Unshift:", fruits);

                // 3. Removing Elements
                fruits.pop(); // Removes the last element
                document.write("After Pop:", fruits);

                fruits.shift(); // Removes the first element
                document.write("After Shift:", fruits);

                // 4. Finding an Element
                let index = fruits.indexOf("Banana");
                document.write("Index of 'Banana':", index);

                let notFound = fruits.indexOf("Grapes"); // Returns -1 if not found
                document.write("Index of 'Grapes':", notFound);

                // 5. Checking if an Element Exists
                let hasCherry = fruits.includes("Cherry");
                document.write("Array includes 'Cherry':", hasCherry);

                // 6. Modifying Elements
                fruits[1] = "Strawberry"; // Replace the second element
                document.write("After Modification:", fruits);


                // 7. Join - Converts array to string
                let joinedString = fruits.join(", ");
                console.log("Joined String:", joinedString);

                // 8. Split - Converts string back to array
                let splitArray = joinedString.split(", ");
                console.log("Split Back to Array:", splitArray);

        // 8 . Functions
                // 1. What are Functions?
                // Functions are reusable blocks of code designed to perform specific tasks.

                // 2. How to Create Functions?
                
                // a. Function Declaration
                function greet(name) {
                    return `Hello, ${name}!`;
                }
                document.write(greet("Alice"));

                // b. Function Expression
                const add = function (a, b) {
                    return a + b;
                };
                document.write(`Addition: ${add(5, 10)}`);

                // c. Arrow Function (introduced in ES6)
                const multiply = (a, b) => a * b;
                document.write(`Multiplication: ${multiply(4, 7)}`);

                // d. Anonymous Function
                setTimeout(function () {
                    document.write("Anonymous Function Executed After 2 Seconds");
                }, 2000);

                // 3. Parameters and Arguments
                function describePerson(name, age) {
                    document.write(`Name: ${name}, Age: ${age}`);
                }
                describePerson("Bob", 30); // Passing arguments

                // 4. Default Parameters
                function greetWithDefault(name = "Guest") {
                    return `Hello, ${name}!`;
                }
                document.write(greetWithDefault());
                document.write(greetWithDefault("Charlie"));

                // 5. Return Values
                function calculateSquare(number) {
                    return number * number;
                }
                document.write(`Square: ${calculateSquare(6)}`);

                // 6. Function Scope
                let globalVar = "I am global";
                function scopeExample() {
                    let localVar = "I am local";
                    document.write(globalVar); // Can access global variables
                    document.write(localVar); // Can access local variables
                }
                scopeExample();
                document.write(localVar); // Error: localVar is not defined
    </script>
</body>
</html>
```
       

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript Inline Events</title>
    <style>
        button, input {
            margin: 10px;
            padding: 10px;
            font-size: 16px;
        }
        div {
            width: 200px;
            height: 100px;
            background-color: lightblue;
            text-align: center;
            line-height: 100px;
            margin: 10px;
        }
    </style>
</head>
<body>
    <h1>JavaScript Inline Event Examples</h1>

    <!-- Event Examples -->
    <button onclick="handleClick()">Click Me</button>
    <input type="text" id="textInput" onchange="handleChange(event)" onblur="handleBlur()" placeholder="Type something...">
    <div onmouseover="handleMouseOver()" onmouseout="handleMouseOut()" id="hoverDiv">Hover Over Me</div>
    <div ondblclick="handleDoubleClick()">Double-Click Me</div>
    <button onclick="handleFocus()">Focus Input</button>
    <div onmousedown="handleMouseDown()" onmouseup="handleMouseUp()">Mouse Events Here</div>
    <button onkeypress="handleKeyPress(event)">Press Key</button>

    <!-- Form Submission -->
    <form onsubmit="handleSubmit(event)">
        <input type="text" placeholder="Name">
        <button type="submit">Submit</button>
    </form>

    <script>
        // Function Definitions

        // 1. Click Event
        function handleClick() {
            alert("Button Clicked!");
        }

        // 2. Input Change Event
        function handleChange(event) {
            document.write("Input Changed:", event.target.value);
        }

        // 3. Mouseover Event
        function handleMouseOver() {
            const hoverDiv = document.getElementById("hoverDiv");
            hoverDiv.style.backgroundColor = "lightgreen";
        }

        // 4. Mouseout Event
        function handleMouseOut() {
            const hoverDiv = document.getElementById("hoverDiv");
            hoverDiv.style.backgroundColor = "lightblue";
        }

        // 5. Double-Click Event
        function handleDoubleClick() {
            alert("Div Double-Clicked!");
        }

        // 6. Focus Event
        function handleFocus() {
            const input = document.getElementById("textInput");
            input.focus();
        }

        // 7. Keypress Event
        function handleKeyPress(event) {
            document.write(`Key Pressed: ${event.key}`);
        }

        // 8. Mouse Down and Mouse Up Events
        function handleMouseDown() {
            const mouseDiv = document.querySelector("div[onmousedown]");
            mouseDiv.textContent = "Mouse Down!";
            mouseDiv.style.backgroundColor = "orange";
        }

        function handleMouseUp() {
            const mouseDiv = document.querySelector("div[onmousedown]");
            mouseDiv.textContent = "Mouse Events Here";
            mouseDiv.style.backgroundColor = "lightblue";
        }

        // 9. Blur Event
        function handleBlur() {
            document.write("Input Lost Focus!");
        }

        // 10. Submit Event
        function handleSubmit(event) {
            event.preventDefault(); // Prevent the form from submitting
            alert("Form Submitted!");
        }
    </script>
</body>
</html>
```

Here's a simple example of form validation without using regular expressions. This example checks for basic conditions like empty fields, email structure (using a basic `indexOf` check), and password length.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Form Validation</title>
    <style>
        form {
            max-width: 300px;
            margin: 20px auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        input {
            display: block;
            width: 100%;
            margin: 10px 0;
            padding: 8px;
            font-size: 16px;
        }
        .error {
            color: red;
            font-size: 14px;
        }
    </style>
</head>
<body>
    <h1>Simple Form Validation</h1>
    <form onsubmit="return validateForm()">
        <label for="username">Username:</label>
        <input type="text" id="username" placeholder="Enter your username">
        <span id="usernameError" class="error"></span>

        <label for="email">Email:</label>
        <input type="text" id="email" placeholder="Enter your email">
        <span id="emailError" class="error"></span>

        <label for="password">Password:</label>
        <input type="password" id="password" placeholder="Enter your password">
        <span id="passwordError" class="error"></span>

        <button type="submit">Submit</button>
    </form>

    <script>
        function validateForm() {
            // Get input values
            const username = document.getElementById("username").value.trim();
            const email = document.getElementById("email").value.trim();
            const password = document.getElementById("password").value.trim();

            // Get error display elements
            const usernameError = document.getElementById("usernameError");
            const emailError = document.getElementById("emailError");
            const passwordError = document.getElementById("passwordError");

            // Reset error messages
            usernameError.textContent = "";
            emailError.textContent = "";
            passwordError.textContent = "";

            let isValid = true;

            // Validate Username
            if (username === "") {
                usernameError.textContent = "Username cannot be empty.";
                isValid = false;
            }

            // Validate Email (basic check)
            if (email === "") {
                emailError.textContent = "Email cannot be empty.";
                isValid = false;
            } else if (email.indexOf("@") === -1 || email.indexOf(".") === -1) {
                emailError.textContent = "Enter a valid email address.";
                isValid = false;
            }

            // Validate Password
            if (password === "") {
                passwordError.textContent = "Password cannot be empty.";
                isValid = false;
            } else if (password.length < 6) {
                passwordError.textContent = "Password must be at least 6 characters long.";
                isValid = false;
            }

            // Return false to prevent form submission if validation fails
            return isValid;
        }
    </script>
</body>
</html>
```

Here’s an example of form validation using **regular expressions (regex)** to validate inputs like username, email, and password. Regular expressions allow for pattern matching, making validation more precise.

---

### Code Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Validation with Regex</title>
    <style>
        form {
            max-width: 300px;
            margin: 20px auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        input {
            display: block;
            width: 100%;
            margin: 10px 0;
            padding: 8px;
            font-size: 16px;
        }
        .error {
            color: red;
            font-size: 14px;
        }
    </style>
</head>
<body>
    <h1>Form Validation with Regex</h1>
    <form onsubmit="return validateForm()">
        <label for="username">Username:</label>
        <input type="text" id="username" placeholder="Enter your username">
        <span id="usernameError" class="error"></span>

        <label for="email">Email:</label>
        <input type="text" id="email" placeholder="Enter your email">
        <span id="emailError" class="error"></span>

        <label for="password">Password:</label>
        <input type="password" id="password" placeholder="Enter your password">
        <span id="passwordError" class="error"></span>

        <button type="submit">Submit</button>
    </form>

    <script>
        function validateForm() {
            // Get input values
            const username = document.getElementById("username").value.trim();
            const email = document.getElementById("email").value.trim();
            const password = document.getElementById("password").value.trim();

            // Get error display elements
            const usernameError = document.getElementById("usernameError");
            const emailError = document.getElementById("emailError");
            const passwordError = document.getElementById("passwordError");

            // Reset error messages
            usernameError.textContent = "";
            emailError.textContent = "";
            passwordError.textContent = "";

            let isValid = true;

            // Regex Patterns
            const usernamePattern = /^[a-zA-Z0-9_]{3,15}$/; // Letters, numbers, underscores; 3-15 characters
            const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/; // Basic email validation
            const passwordPattern = /^(?=.*[A-Za-z])(?=.*\d)[A-Za-z\d]{6,}$/; // At least 6 chars, 1 letter, 1 number

            // Validate Username
            if (!usernamePattern.test(username)) {
                usernameError.textContent = "Username must be 3-15 characters, letters, numbers, or underscores.";
                isValid = false;
            }

            // Validate Email
            if (!emailPattern.test(email)) {
                emailError.textContent = "Enter a valid email address.";
                isValid = false;
            }

            // Validate Password
            if (!passwordPattern.test(password)) {
                passwordError.textContent = "Password must be at least 6 characters, include 1 letter and 1 number.";
                isValid = false;
            }

            // Return false to prevent form submission if validation fails
            return isValid;
        }
    </script>
</body>
</html>
```

---

### Explanation of Regex Patterns

1. **Username Pattern**: 
   ```regex
   /^[a-zA-Z0-9_]{3,15}$/
   ```
   - `^` and `$`: Start and end of the string.
   - `[a-zA-Z0-9_]`: Allows letters, numbers, and underscores.
   - `{3,15}`: The length of the username should be between 3 and 15 characters.

2. **Email Pattern**:
   ```regex
   /^[^\s@]+@[^\s@]+\.[^\s@]+$/
   ```
   - `^[^\s@]+`: Starts with one or more characters that are not spaces (`\s`) or `@`.
   - `@`: Requires an `@` symbol.
   - `[^\s@]+\.[^\s@]+`: Requires a domain with a dot (`.`) and a valid ending (e.g., `.com`, `.org`).

3. **Password Pattern**:
   ```regex
   /^(?=.*[A-Za-z])(?=.*\d)[A-Za-z\d]{6,}$/
   ```
   - `(?=.*[A-Za-z])`: Requires at least one letter.
   - `(?=.*\d)`: Requires at least one digit.
   - `[A-Za-z\d]{6,}`: Password must be at least 6 characters long.

---

### How to Use Regex

- **Pattern Matching**: Use `pattern.test(value)` to check if a string matches the pattern.
- **Dynamic Validation**: Regex provides more control and precision compared to simple string checks.
- **Errors and Feedback**: Show meaningful error messages if patterns are not matched.

---

### Why Use Regex?

- Regex simplifies complex string validations.
- It's reusable and compact for various input types.
- Ideal for email, password, or custom format checks.

Test this form in your browser, and experiment with invalid and valid inputs to observe how regex helps in validation.







