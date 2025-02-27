# JavaScript Essentials & VS Code Shortcuts - A Developer's Guide

## Introduction
JavaScript is one of the most widely used programming languages for web development. Whether you're a beginner or an experienced developer, understanding JavaScript concepts and leveraging VS Code shortcuts can significantly enhance your productivity. This guide covers key JavaScript fundamentals with well-documented code snippets and important VS Code features that streamline the development process.

---

## **VS Code Features & Shortcuts**
- **`Ctrl + F`** → Search for specific text in an entire file, similar to searching messages in WhatsApp.
- **`Ctrl + I`** → Activate GitHub Copilot.
- **`Ctrl + .`** → Generate code using Copilot.

---

## **JavaScript Basics**
### 1. **Logging Output to the Console**
```js
console.log(`Hello`);
console.log(`I Like Pizza`);
```

### 2. **Displaying Alerts and Updating HTML Content**
```js
window.alert(`This Is An Alert`);
document.getElementById("myH1").textContent = `Hello`;
document.getElementById("myP").textContent = `I Like Pizza`;
```

### 3. **Comments in JavaScript**
```js
// This Is A Single-line Comment

/* This
   Is
   A
   Multi-line
   Comment */
```

---

## **Variables in JavaScript**
### **Declaration & Assignment**
```js
let age = 25;
console.log(`You Are ${age} Years Old`);
console.log(typeof age);

let Name = `Surya`;
console.log(typeof Name);
```

### **Boolean Data Type**
```js
let online = true;
console.log(online);
console.log(typeof online);
```

### **Displaying Variables in HTML**
```js
let fullName = "Surya";
let age = 25;
let student = false;

document.getElementById("p1").textContent = `Your Name Is: ${fullName}`;
document.getElementById("p2").textContent = `Your Age Is: ${age}`;
document.getElementById("p3").textContent = `Enrolled: ${student}`;
```

---

## **Mathematical Operations & Operator Precedence**
### **Augmented Assignment Operators**
Examples: `+=`, `-=`, `*=`, `/=`

### **Operator Precedence Order**
1. Parentheses `()`
2. Exponents `**`
3. Multiplication, Division, Modulus `* / %`
4. Addition & Subtraction `+ -`

```js
let result = 1 + 2 * 3 + 4 ** 2;
console.log(result);

let result = 12 % 5 + 8 / 2;
console.log(result);
```

---

## **User Input in JavaScript**
### 1. **Easy Way - `window.prompt`**
```js
let username;
username = window.prompt("What's Your UserName ?");
console.log(username);
```

### 2. **Professional Way - HTML Textbox**
```js
let username;
document.getElementById("mySubmit").onclick = function(){
    username = document.getElementById("myText").value;
    console.log(username);
    document.getElementById("myH1").textContent = `Hello ${username}`;
};
```

---

## **Type Conversion in JavaScript**
```js
let Age;
Age = window.prompt("How Old Are You ?");
Age = Number(Age);
Age += 1;
console.log(Age);
```

```js
let x = "Pizza";
let y = "Pizza";
let z = "Pizza";

x = Number(x);
y = String(y);
z = Boolean(z);

console.log(x, typeof x);
console.log(y, typeof y);
console.log(z, typeof z);
```

---

## **Constants in JavaScript**
```js
const PI = 3.14;
console.log(PI);
```

```js
document.getElementById("mySubmit").onclick = function(){
    Value = document.getElementById("myText").value;
    Value = Number(Value);
    Value = PI * Value ** 2;
    document.getElementById("myH3").textContent = Value;
};
```

---

## **Random Number Generator**
```js
const min = 1;
const max = 7;
let RandomNum = Math.floor(Math.random() * (max - min)) + min;
console.log(RandomNum);
```

---

## **Conditional Statements in JavaScript**
### **Using `if-else` Statements**
```js
let Age = 25;
if(Age >= 18){
   console.log("You Are Old Enough To Enter This Site");
} else {
   console.log("Don't Enter...!!");
}
```

---

## **Ternary Operator (`? :`)**
```js
let Age = 21;
let Check = Age >= 18 ? "You Are An Adult" : "You Are Not An Adult";
console.log(Check);
```

---

## **String Methods in JavaScript**
```js
let UserName = "Surya Is A SDE";
console.log(UserName.toUpperCase());
console.log(UserName.toLowerCase());
console.log(UserName.includes("SDE"));
```

```js
let PhoneNumber = `123-456-789`;
PhoneNumber = PhoneNumber.replaceAll("-", "");
console.log(PhoneNumber);
```

---

## **String Slicing in JavaScript**
```js
const FullName = "Surya Code";
let FirstName = FullName.slice(0, FullName.indexOf(" "));
let LastName = FullName.slice(FullName.indexOf(" ") + 1);
console.log(FirstName);
console.log(LastName);
```

---

## **Method Chaining**
```js
let UserName = window.prompt("Enter Your Username: ");
UserName = UserName.trim();

let Letter = UserName.charAt(0);
Letter = Letter.toUpperCase();

let ExtraChars = UserName.slice(1);
ExtraChars = ExtraChars.toLowerCase();

let Sum = Letter + ExtraChars;
console.log(Sum);
```

---

# Mastering JavaScript: Essential Concepts and Code Examples

JavaScript is a powerful language used for web development. Whether you're a beginner or an experienced developer, understanding fundamental concepts is crucial for writing clean and efficient code. This blog explores some essential JavaScript concepts with practical examples.

---

## No Method Chaining in JavaScript
When working with strings, method chaining allows for concise transformations. However, avoiding chaining can sometimes improve readability.

```javascript
let UserName = window.prompt("Enter Your Username : ");
UserName = UserName.trim().charAt(0).toUpperCase() + UserName.trim().slice(1).toLowerCase();
console.log(UserName);
```

This ensures the first letter is capitalized while the rest remain lowercase, maintaining proper formatting.

---

## Logical and Comparison Operators

### Logical Operators:
1. **AND (`&&`)**
2. **OR (`||`)**
3. **NOT (`!`)** (Example: `Valid = false; if (!Valid) { // Executes }`)

### Comparison Operators:
- `=`: Assignment Operator
- `==`: Loose Comparison (Only compares values, ignores data type)
- `===`: Strict Comparison (Compares both value and data type)
- `!=`: Inequality Operator
- `!==`: Strict Inequality Operator

#### Example:
```javascript
console.log(3.14 == "3.14"); // true
console.log(3.14 === "3.14"); // false
```

---

## Understanding While Loops

### Simple While Loop Example:
```javascript
let UserName = "";
while (UserName === "") {
   UserName = window.prompt("Enter some UserName : ");
}
console.log(UserName);
```
If "Cancel" is pressed, `null` is returned. To prevent this:
```javascript
while (UserName === "" || UserName === null) {
   UserName = window.prompt("Enter some UserName : ");
}
```
This ensures a valid username is entered before proceeding.

---

## User Authentication Example
```javascript
let Bool = false;
let UserName, Password;
while (!Bool) {
   UserName = window.prompt("Enter Your UserName :");
   Password = window.prompt("Enter Your Password :");
   if (UserName === "MyUserName" && Password === "MyPassword") {
       Bool = true;
       console.log("Done JS Coder...!! You Are Logged-In");
   } else {
       console.log("Done Some Mistakes In Log-In");
   }
}
```

---

## Number Guessing Game
A simple game where the user guesses a number between 1 and 100.
```javascript
const minNum = 1;
const maxNum = 100;
const Answer = Math.floor(Math.random() * (maxNum - minNum + minNum)) + minNum;
let Attempts = 0;
let Guess;
let Attempt = true;
while (Attempt) {
    Guess = window.prompt(`Guess A Number Between ${minNum} And ${maxNum}`);
    Guess = Number(Guess);
    if (isNaN(Guess)) {
        window.alert("Enter A Valid Number");
    } else if (Guess < minNum || Guess > maxNum) {
        window.alert("Enter A Valid Number");
    } else {
        Attempts++;
        if (Guess < Answer) {
            window.alert("Too Low...!!");
        } else if (Guess > Answer) {
            window.alert("Too High...!!");
        } else {
            window.alert(`You Got It Correct...!! In ${Attempts} Attempts`);
            Attempt = false;
        }
    }
}
```

---

## Functions and Scope
```javascript
function Surya(UserName, Date) {
   console.log(`Hi ${UserName}`);
   console.log(`Your Birthday Is Next Month By ${Date}`);
}
Surya("Surya", 5);
Surya("Dharshana", 28);
```

Scope Example:
```javascript
let x = 5;
function Example1() {
   let x = 10;
   console.log(x);
}
function Example2() {
   let x = 50;
   console.log(x);
}
Example1();  // 10
Example2();  // 50 (Local scope takes precedence)
```

---

## Arrays and Operations

### Basic Array Operations:
```javascript
let fruits = ["Apple", "Carrot", "Banana"];
fruits[0] = "Changed";
fruits[4] = "New Index";
console.log(fruits);
```

### Push, Pop, Unshift, and Shift:
```javascript
fruits.push("Pushed New To End");
fruits.pop();
fruits.unshift("Surya");
fruits.shift();
console.log(fruits);
```

### Looping through Arrays:
```javascript
for (let fruit of fruits) {
    console.log(fruit);
}
```

---

## Sorting and Spread Operator
Sorting an array:
```javascript
let Sorted_Array = fruits.sort();
console.log(Sorted_Array);
Sorted_Array = fruits.sort().reverse();
console.log(Sorted_Array);
```

Using the spread operator:
```javascript
let Numbers = [1, 2, 3, 4, 5];
let Maximum = Math.max(...Numbers);
console.log(Maximum); // 5
```

---

## Rest Parameters in Functions

Handling multiple arguments:
```javascript
function Open_Fridge(...Foods) {
    console.log(Foods);
}
Open_Fridge("Pizza", "Burger", "HotDog");
```

Summing multiple numbers:
```javascript
function Sum(...Numbers) {
   let sum = 0;
   for (let number of Numbers) {
       sum += number;
   }
   return sum;
}
console.log(Sum(1, 3, 4, 2));
```

Merging multiple strings:
```javascript
function Merge(...Strings) {
    return Strings.join(" ");
}
console.log(Merge("Surya", "Is", "a", "SDE"));
```

---
# JavaScript Projects and Concepts

## Dice Game

### Functionality
The Dice Game allows users to roll a dice multiple times and display the corresponding images of the rolled numbers.

```javascript
function Roll(){
   const UserValue = document.getElementById("InputBox").value;
   const Result = document.getElementById("Result");
   const Images = document.getElementById("Images");
   const Result_Array = [];
   const Images_Array = [];

   for(let i = 0; i < UserValue ; i++){
      const Random_Number = Math.floor(Math.random()*6)+1;
      Result_Array.push(Random_Number);
      Images_Array.push(`<img src="Images/${Random_Number}.png">`)
   }
   Result.textContent = `Dice : ${Result_Array.join(" , ")}`;
   Images.innerHTML = Images_Array.join(" ");
}
```

**Example Output (User inputs 3):**
```
Dice: 4, 2, 6
(Images displayed corresponding to rolled numbers)
```

## Random Password Generator

### Functionality
This function generates a random password based on user-selected parameters.

```javascript
function generatePassword(length , includeUpperCase , includeLowerCase , includeNumbers , includeSymbols){
   const upperCaseChars = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
   const lowerCaseChars = "abcdefghijklmnopqrstuvwxyz";
   const numberchars = "0123456789";
   const symbolChars = "!@#$%^&*()_+-\|/?";

   let allowedChars = "";
   let password = "";

   allowedChars += includeUpperCase ? upperCaseChars : "";
   allowedChars += includeLowerCase ? lowerCaseChars : "";
   allowedChars += includeNumbers ? numberchars : "";
   allowedChars += includeSymbols ? symbolChars : "";

   if(length <= 0){
      return `(Password Length Must Be Atleast One)`;
   }
   if(allowedChars.length === 0){
      return `(Atleast 1 Set Of Characters Need To Be Selected)`;
   }
   for(let i = 0; i < length ; i++){
      const randomIndex = Math.floor(Math.random() * allowedChars.length);
      password += allowedChars[randomIndex];
   }
   return password;
}
```

**Example usage:**
```javascript
const passwordLength = 8;
const includeUpperCase = true;
const includeLowerCase = true;
const includeNumbers = true;
const includeSymbols = false;

const password = generatePassword(passwordLength , includeUpperCase , includeLowerCase , includeNumbers , includeSymbols);
console.log(`Generated Password : ${password}`);
```

**Example Output:**
```
Generated Password: AbxT92hd
```

## JavaScript Concepts

### Callback Functions
A callback function is passed as an argument to another function, often used in asynchronous operations such as:
1. Reading a file
2. Network requests
3. Interacting with databases

Example:
```javascript
hello(goodBye);
function hello(callback){
   console.log(`Hello...!!`);
   callback();
}
function goodBye(){
   console.log(`Goodbye...!!`);
}
```
**Output:**
```
Hello...!!
Goodbye...!!
```

### forEach() Method
Used to iterate over an array and apply a specified function to each element.

Example:
```javascript
let numbers = [1 , 2 , 3 , 4 , 5];
numbers.forEach(display);
function display(element){
   console.log(element);
}
```
**Output:**
```
1
2
3
4
5
```

### .map() Method
Creates a new array by applying a function to each element.

Example:
```javascript
const numbers = [1 , 2 , 3 , 4 , 5];
const squares = numbers.map(square);
console.log(squares);
function square(element){
   return Math.pow(element,2);
}
```
**Output:**
```
[1, 4, 9, 16, 25]
```

### .filter() Method
Creates a new array by filtering elements based on a condition.

Example:
```javascript
let numbers = [1 , 2 , 3 , 4 , 5 , 6 , 7];
let Filtered_Numbers = numbers.filter(even_number);
console.log(Filtered_Numbers);
function even_number(element){
   return element % 2  === 0;
}
```
**Output:**
```
[2, 4, 6]
```

### .reduce() Method
Reduces an array to a single value using an accumulator.

Example:
```javascript
const prices = [10 , 70 , 80];
let sum_of_prices = prices.reduce(sum);
console.log(`$${sum_of_prices}`);
function sum(accumulator , element){
   return accumulator + element;
}
```
**Output:**
```
$160
```

### Arrow Functions
A more concise way to write function expressions.

Example:
```javascript
const hello = () => console.log("Hello...!!");
hello();
```
**Output:**
```
Hello...!!
```

### Object and `this` keyword
Objects represent a collection of related properties and methods.

Example:
```javascript
const person = {
    firstName : "Surya",
    lastName : "PR",
    age : 17,
    isEmployed : true,
}
console.log(person.firstName);
console.log(person.age);
```
**Output:**
```
Surya
17
```

Using `this` keyword:
```javascript
const this_var = {
    name : "Spongebob",
    age : 25,
    funct_call : function(){
        console.log(`${this.name} Is ${this.age} Years Old`);
    }
}
this_var.funct_call();
```
**Output:**
```
Spongebob Is 25 Years Old
```

### Classes and Objects
A class provides a structured way to define objects.

Example:
```javascript
class Product {
    constructor(name, age){
        this.name = name;
        this.age = age;
    }
    displayProduct(){
        console.log(`Name: ${this.name}`);
        console.log(`Age: ${this.age}`);
    }
}
const store = new Product("Surya", 17);
store.displayProduct();
```
**Output:**
```
Name: Surya
Age: 17
```

### Static Keyword
Defines properties or methods that belong to a class itself rather than instances.

Example:
```javascript
class MathUtil{
    static PI = 3.14;
}
console.log(MathUtil.PI);
```
**Output:**
```
3.14
```

### Inheritance
Allows a new class to inherit properties and methods from an existing class.

Example:
```javascript
class Animal {
    alive = true;
    eat(){
        console.log("This animal is eating.");
    }
}
class Rabbit extends Animal {
    name = "Rabbit";
}
const bunny = new Rabbit();
bunny.eat();
```
**Output:**
```
This animal is eating.
```







