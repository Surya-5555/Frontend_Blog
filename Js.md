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

## **Conclusion**
Mastering JavaScript and leveraging VS Code shortcuts can help improve coding efficiency. This guide provides a solid foundation for JavaScript fundamentals, from variables and mathematical operations to user input handling and method chaining. Keep experimenting and enhancing your skills for better development experience!

---

