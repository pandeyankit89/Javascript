## Javascript

### Why we don't use ```var``` anymore and difference between ```let``` and ```const``` ?

| Feature | Meaning | `var` (Avoid) | `let` (Use for variables) | `const` (Use for constants) |
|---------|---------|--------------|--------------------|------------------|
| **Scope** | Where the variable is accessible  | Function-scoped ( exists outside of {} also) | Block-scoped ✅  ( exists only inside of {})| Block-scoped ✅  ( exists only inside of {}) |
| **Redeclaration** | Can we define the same variable name again? | ✅ Allowed (causes bugs) | ❌ Not allowed | ❌ Not allowed |
| **Reassignment** | Can we change the value after defining it? | ✅ Allowed | ✅ Allowed | ❌ Not allowed |
| **Hoisting** | Does JavaScript move the declaration to the top? | ✅ Hoisted with `undefined` | ✅ Hoisted (but error if accessed before assignment) | ✅ Hoisted (but error if accessed before assignment) |

---

```javascript
// How to Declare a Variable:
let camelCaseVariable123WhichCanOnlyHaveTwoSpecialCharacters$and_;
```

### How to Take Input from User
```javascript
camelCaseVariable123WhichCanOnlyHaveTwoSpecialCharacters$and_ = prompt("What is your name ?");
```

### How to Show a Screen Popup Output
```javascript
alert("Your name is " + camelCaseVariable123WhichCanOnlyHaveTwoSpecialCharacters$and_ );
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
let i = 1;
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
If there is an anchor element as ```<a id="myLink" href="https://example.com" target="_blank">Click me</a>```
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
- Example : For ```<p id="myPara" class="info">Hello, <b>World!</b></p>```
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
### **Object**
- An ```object``` is a collection of related ```data (properties)``` and ```functions (methods)```. It helps in organizing data better.
- ```Properties``` are key-value pairs inside an object.
	- You can access properties in two ways:
		- *Dot notation*: ```person.name```
		- *Bracket notation*: ```person["age"]```
- A ```method``` is a function inside an object.
		
```javascript
	let object_name = {
		property_1: "John",
		property_1: 30,
		property_3: "New York" ,
		// Note : method name not having "()" at end.
		method_name: function() { 
					return "Hello, my name is " + this.property_1;
				} 		// Note : No comma (,) in last												
	
	};
	console.log(object_name);  // Outputs: { property_1: 'John', property_2: 30, property_3: 'New York' }
	console.log(object_name.property_1);   	// John
	console.log(object_name["property_2"]); // 30
	console.log(object_name.method_name()); // Outputs: "Hello, my name is John" Note: calling method with "()" at end.
```

- Adding/Updating Properties:
```javascript
	object_name.property_4 = "USA"; 	// Adds a new property
	object_name.property_2 = 31;        // Updates existing property
```
---
### **this**

- keyword ```this``` refers to the object it belongs to.
- *Inside an Object*

```javascript
	let car = {
		brand: "Toyota",
		model: "Corolla",
		showInfo: function() {
			console.log("Car: " + this.brand + " " + this.model);
		}
	};
	car.showInfo(); // Car: Toyota Corolla
	// Here, this.brand and this.model refer to car.brand and car.model.
```
- ```this``` in Global Scope
```javascript
	console.log(this);  
	// In browser, "this" refers to the `window` object
```
- ```this``` in a Function
```javascript
	function show() {
		console.log(this);  
	}
	show();
	// In a normal function, "this" refers to the global object (window in browsers).	
```
- ```this``` in an Event Listener
```javascript
	let button = {
		text: "Click Me",
		click: function() {
			console.log("Button Text: " + this.text);
		}
	};
	button.click();  // Output: Button Text: Click Me
	// Here, this.text refers to button.text.
```
---
### **constructor**
- A ```constructor``` is a special function used to create multiple objects with the same structure and properties.
- Instead of manually creating objects, We can use a ```constructor function``` to create multiple objects dynamically.
- Starts with a capital letter by convention, like ```function MyConstructor()```
- Uses ```this``` to assign properties.
- Uses ```new``` to create objects.
```javascript
	function Person(name, age) {  //Name starts with a capital letter by convention. Person, not person.
		this.name = name;
		this.age = age;
		this.greet = function() {
			console.log("Hello, my name is " + this.name);
		};
	}
	
	// Creating objects using the constructor
	let person1 = new Person("John", 30);
	let person2 = new Person("Alice", 25);
	
	console.log(person1.name);  // Output: John
	console.log(person2.age);   // Output: 25
	
	person1.greet();  // Output: Hello, my name is John
	person2.greet();  // Output: Hello, my name is Alice
```
- Instead of defining functions inside the constructor (which creates a new function for every object), we use ```prototype```.
- Why to use ```prototype``` ?
	- *Without prototype:* Every object gets its own copy of the function.
	- *With prototype:* The function is shared among all objects, saving memory.
---
### 1. Higher-Order Function
A **higher-order function** is a function that **takes another function as an argument or returns a function**.  


```javascript
function greet(name, callback) {
    console.log("Hello, " + name);
    callback(); // Calling the callback function
}

function sayGoodbye() {
    console.log("Goodbye!");
}

// Passing sayGoodbye as a callback to greet
greet("Alice", sayGoodbye);
```
### 2. ```callback``` Function
A **callback function** is a function that is **passed as an argument to another function and executed later**.  
```javascript
function showMessage() {
    console.log("This message appears after 2 seconds!");
}

setTimeout(showMessage, 2000); // Passing showMessage as a callback
```
When you press a key, a callback function is triggered.

###Example: Detecting keypress and executing a callback
```javascript
document.addEventListener("keypress", function(event) {
    console.log("Key pressed: " + event.key);
});
```
- ```document.addEventListener("keypress", function(event) {...})``` registers an event listener.
- When a key is pressed, the anonymous function (callback) executes.
- ```event.key``` gives the key that was pressed.
---
### MediaRecorder API

- Browser has an API feature called MediaRecorder which helps to record audio and/or video from a user's microphone or webcam.
- We can use this ```MediaRecorder``` API feature using JS to create recorder applications.
- There will 2 thhings :
	- Media stream – usually from ```navigator.mediaDevices.getUserMedia()``` (microphone or webcam).
	- MediaRecorder – to record that stream. 
- How to Start recording ```mediaRecorder.start();```. While recording :

(1) First Check User Permission, once start-button is clicked :
```javascript
document.getElementById("start").onclick = async () => {
const stream = await navigator.mediaDevices.getUserMedia({ audio: true });
//Screen: using navigator.mediaDevices.getDisplayMedia() (for screen recording)
```
(2) Disable the start-button and Enable the Stop-button :
```javascript
document.getElementById("startBtn").disabled = true;
document.getElementById("stopBtn").disabled = false;
```
(3) Once permission received, start the recording -
```javascript
	mediaRecorder = new MediaRecorder(stream);
	mediaRecorder.start();
```
(4) We store these recording streams in chunks using ```mediaRecorder.ondataavailable`` eventin an array.
```javascript
	audioChunks = [];
	mediaRecorder.ondataavailable = (event) => {
		audioChunks.push(event.data);
	};
```
(5) When Use clicked "stop-recording button". While Stoppoing, convert the chunks into Blob, which can use it like a source which we can play using ```audio``` tag.
```javascript
	mediaRecorder.onstop = () => {
		const audioBlob = new Blob(audioChunks, { type: 'audio/webm' });
		const audioUrl = URL.createObjectURL(audioBlob);
		document.getElementById("audioPlayback").src = audioUrl;
	};
```
- How to Stop recording ```mediaRecorder.stop();```. While stopping :
  
(1) Stop the recording once stop-button is clicked :
```javascript
	document.getElementById("stop").onclick = () => {
		mediaRecorder.stop();
	};
```
(2) Enable the start-button and Disable the Stop-button :
```javascript
	document.getElementById("startBtn").disabled = false;
	document.getElementById("stopBtn").disabled = true;
```
### Complete script is here => [myAudioRecorder.html](myAudioRecorder.html)
![myAudioRecorder Page](myAudioRecorder.png)
---
