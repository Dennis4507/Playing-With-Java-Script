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
```html
<script>
    let name = "John";
    let surname = "Doe";
    let age = 11;
    age = 54; // Reassigning the value of `age`
    let isStudent = true;

    // Notice the lack of `let` on line 14 - we don’t need it since the variable has already been declared earlier and we are just re-assigning it here
</script>
```

---

## Adding Interactivity with the DOM

We added functionality to dynamically update the content of a webpage using JavaScript and the DOM (Document Object Model). Below is a summary of what we implemented:

### HTML Structure
We created a simple HTML structure with a button and a paragraph element:
```html
<h1>JavaScript String Method</h1>
<p>Convert String to Upper case:</p>
<button onclick="myFunction()">Try it</button>
<p id="demo">Hello World!</p>
```

### JavaScript Code
We wrote a JavaScript function to convert the text inside the paragraph element with the `id="demo"` to uppercase when the button is clicked:
```javascript
function myFunction() {
    // Get the text from the paragraph element with id "demo"
    let text = document.getElementById("demo").innerHTML;
    // Convert the text to uppercase and update the paragraph content
    document.getElementById("demo").innerHTML = text.toUpperCase();
}
```

---

## How It Works

1. The `onclick` attribute in the `<button>` element calls the `myFunction()` function when the button is clicked.
2. Inside the function:
   - `document.getElementById("demo").innerHTML` retrieves the current text content of the paragraph element with the `id="demo"`.
   - The `toUpperCase()` method converts the text to uppercase.
   - The updated text is assigned back to the `innerHTML` property of the same paragraph element, dynamically updating the content on the webpage.

---

## Debugging and Fixes

### Issue
Initially, the code did not work as expected because the `<script>` tag was placed before the DOM was fully loaded. This caused the `document.getElementById("demo")` call to fail.

### Solution
To fix this, we ensured that the `<script>` tag was placed at the end of the `<body>` section, just before the closing `</body>` tag. This ensures that the DOM is fully loaded before the JavaScript code runs:
```html
<script>
    function myFunction() {
        let text = document.getElementById("demo").innerHTML;
        document.getElementById("demo").innerHTML = text.toUpperCase();
    }
</script>
</body>
```

---

## Final Output

When the button is clicked, the text "Hello World!" in the paragraph is dynamically converted to "HELLO WORLD!" without reloading the page.

This demonstrates how JavaScript can be used to create interactive and dynamic web pages by manipulating the DOM.

