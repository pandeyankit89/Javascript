## Javascript

```javascript
// How to Declare a Variable:
var CamelCaseVariable123WhichCanOnlyHaveTwoSpecialCharacters$and_;
```

### How to Take Input from User
```javascript
CamelCaseVariable123WhichCanOnlyHaveTwoSpecialCharacters$and_ = prompt("What is your name ?");
```

### How to Show a Screen Popup Output
```javascript
alert("Your name is " + CamelCaseVariable123WhichCanOnlyHaveTwoSpecialCharacters$and_ );
```

### Data Type of a Variable
```javascript
typeof(myVar);
```

### String Operations
- **Length of a string:** `myVar.length`
- **Substring of a string:** `myVar.slice(0,2);` (From 0th position up to, but not including, the 2nd position)
- **Change string to Upper Case:** `myVar.toUpperCase();`
- **Change string to Lower Case:** `myVar.toLowerCase();`

### Mathematical Operations
```javascript
alert("Data type of division is: " + typeof(5/2) + " (not float), while modulo is: " + typeof(4%2));
```

### Increment & Assignment Operations
- `y = x++;` → x value is assigned first to y before x is incremented.
- `y += 1;` → y will be incremented by 1 and then reassigned to y.

### Printing to Developer Console
```javascript
console.log("myVar is: " + myVar);
```

### Math Functions
- `Math.floor()`
- `Math.ceil()`
- `Math.round()`
- `Math.PI`

### Function Declaration & Calling
```javascript
// Function declaration (no semicolon at end)
function add(a, b) {
    return a + b;
}

// Function calling (semicolon at end)
add(2,3);
```

### Random Number Generation
```javascript
// Math.random() generates a random number between 0 (inclusive) and 1 (not inclusive)
Math.random();

// Random Dice:
Math.floor(Math.random() * 6) + 1;
```

### Comparison Operators
- `===`, `!==`, `&&` (AND), `||` (OR)
- `==` checks for only **value**
- `===` checks for both **value** and **data type**

### Conditional Statements
```javascript
if (x === y) {
    console.log(x + " is equal to " + y);
} else {
    console.log(x + " is not equal to " + y);
}
```

### **Good Example of If-Nesting**: Checking Leap Year

### **FizzBuzz Example**
```javascript
if (count % 3 === 0 && count % 5 === 0) {
    console.log("FizzBuzz");
} else if (count % 3 === 0) {
    console.log("Fizz");
} else if (count % 5 === 0) {
    console.log("Buzz");
} else {
    console.log(count);
}
```

## **JavaScript Arrays**
```javascript
var myArray = ["AA", "BB", "CC", "DD"];
```

- **Accessing a specific value:** `myArray[0];`
- **Checking if an array has a specific value:** `myArray.includes("AA")`
- **Adding a value as the last item:** `myArray.push("EE");`
- **Removing the last value:** `myArray.pop();`

## **Loops in JavaScript**

### While Loop
```javascript
var i = 1;
while (i < 5) {
    console.log(i);
    i++;
}
```

### For Loop
```javascript
for(var i = 0; i < 5; i++) {
    console.log(i);
}
```
**Note:** Use `while` if checking the state, and `for` if iterating.

## **DOM (Document Object Model)**
The DOM is a tree-like representation of an HTML document that allows scripts to dynamically access, modify, and manipulate elements, attributes, and content.

### **Accessing DOM Elements**
```javascript
document.firstElementChild;
document.lastElementChild;
document.firstElementChild.firstElementChild;
document.querySelector("h1");
document.getElementsByTagName("h1");
document.getElementById("id1");
```

### **Changing Style of an Element using JavaScript**
```javascript
document.getElementById("id1").style.color = "red";
document.getElementById("id1").style.backgroundColor = "red";
document.getElementById("id1").style.textAlign = "center";
```
**Note:** CSS style names and JavaScript style names differ:

| **CSS** | **JavaScript** |
|---------|---------------|
| font-size | fontSize |
| text-align | textAlign |
| background-color | backgroundColor |

## **Best Practices**

- **HTML** → Structure
- **CSS** → Style
- **JavaScript** → Behavior

It is recommended to define styles in CSS rather than changing them via JavaScript. Instead of modifying styles directly, add predefined CSS classes dynamically.

### **Adding a Class Dynamically**
```javascript
document.getElementById("id1").classList.add("new-class");
```

### **Checking if an Element Has a Class**
```javascript
document.getElementsByClassName("new-class");
```
---
### **getAttribute("attributeName")**
If there is an anchor element as below -
```html
	<a id="myLink" href="https://example.com" target="_blank">Click me</a>
```
```javscript
console.log(document.getElementById("myLink").getAttribute("href"));  //Output = https://example.com
```


```javscript
console.log(document.getElementById("myLink").getAttribute("target")); //Output =  _blank
```
### **setAttribute("attributeName", "new_value")**
```javscript
document.getElementById("myLink").setAttribute("href", "https://google.com");
```

### **Diffrence in getAttribute and innerHTML**
*getAttribute*
- Works only for __HTML__ attributes, not the content inside an element.
- If the attribute does not exist, it returns __null__.
- Example : For "<p id="myPara" class="info">Hello, <b>World!</b></p>"
```javscript
	console.log(document.getElementById("myPara").getAttribute("class")); // Output: "info"
```
*innerHTML*
- Used to get or set the HTML content inside an element.
- Returns everything inside the opening and closing tag, including HTML elements
```javscript
	console.log(document.getElementById("myPara").innerHTML); // Output: "Hello, <b>World!</b>"
```

### **How to Use querySelectorAll() with element and class**
- Select All Elements by Tag Name :
    ```javscript
    let paragraphs = document.querySelectorAll("p");
```
- Select All Elements by Class Name (if class name is "container"):
```javscript
    let paragraphs = document.querySelectorAll(".container");
```
- Select Elements by Tag Name Within a Specific Class:
```javscript
  let paragraphs = document.querySelectorAll(".container p");
```
- Select Elements by Multiple Classes:
```javscript
    let paragraphs = document.querySelectorAll(".container1 .container2");
```
- Select Elements by ID and Class Combination:
```javscript
    let paragraphs = document.querySelectorAll("#app .card");
```	
---
### **Anonymous function**
- An anonymous function is a function without a name. 
- It is often assigned to a variable, passed as an argument, or used as an immediate function expression.
```javscript
let greet = function() {
    console.log("Hello, World!");
};

greet(); // Output: Hello, World!
```
 
### **Event Listeners in Javascript**
- Event Listener which will trigger when a button will be clicked :
```javscript
     // Add click event listener
    button.addEventListener("click", function() {
        alert("Button clicked!");
    });
```
---
