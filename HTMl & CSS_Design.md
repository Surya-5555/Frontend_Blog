# A Collection of HTML & CSS Projects

## Introduction
In this blog, I will be showcasing multiple HTML & CSS projects that I have worked on. Each project is fully coded and functional, demonstrating different aspects of web development, from simple text formatting to fully responsive navigation bars.

---

## 1. Typing Effect with Search Box

This project creates a typing effect for a heading while also including a simple search box.

### Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Typing Effect with Search Box</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            height: 100vh;
            width: 100vw;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background-color: #1e1e2f;
            color: white;
            font-family: 'Courier New', Courier, monospace;
        }
        h1 {
            font-size: 60px;
            font-weight: 500;
            border-right: 4px solid;
            white-space: nowrap;
            overflow: hidden;
            animation: typing 3s steps(14) forwards, blink 0.5s infinite;
            margin-bottom: 40px;
        }
        @keyframes typing {
            from { width: 0 }
            to { width: 14ch }
        }
        @keyframes blink {
            50% { border-color: transparent }
        }
        input[type="text"] {
            padding: 15px;
            font-size: 18px;
            border: none;
            border-radius: 8px;
            width: 300px;
            outline: none;
            color: #333;
        }
        input[type="text"]::placeholder {
            color: #999;
        }
    </style>
</head>
<body>
    <h1>Surya Is A Boy</h1>
    <input type="text" placeholder="Search...">
</body>
</html>
```

### Output:
A heading with a typing animation effect followed by a search box.

---

## 2. Chessboard Layout

This project builds a basic chessboard layout using HTML & CSS, with chess piece symbols.

### Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chessboard</title>
    <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
    <div class="one">
        <div class="two">&#9820</div>
        <div class="two three">&#9822</div>
        <div class="two">&#9821</div>
        <div class="two three">&#9819</div>
        <div class="two">&#9818</div>
        <div class="two three">&#9821</div>
        <div class="two">&#9822</div>
        <div class="two three">&#9820</div>
    </div>
    <div class="one">
        <div class="two three">&#9823</div>
        <div class="two">&#9823</div>
        <div class="two three">&#9823</div>
        <div class="two">&#9823</div>
        <div class="two three">&#9823</div>
        <div class="two">&#9823</div>
        <div class="two three">&#9823</div>
        <div class="two">&#9823</div>
    </div>
</body>
</html>
```

### Output:
A chessboard layout with properly placed chess pieces.

---

## 3. Simple Form Validation

A basic form validation script that ensures the user fills in the required fields before submitting.

### Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Validation</title>
</head>
<body>
    <form onsubmit="return formvalid()">
        NAME:<input type="text" id="one" ><br><br>
        EMAIL:<input type="email" id="two" ><br><br>
        GENDER:<input type="text" required><br><br>
        AGE:<input type="number" required><br><br>
        <hr><br>
        <input type="submit">   <input type="reset">
    </form>
</body>
<script>
    function formvalid(){
        const one=document.getElementById('one').value;
        const two=document.getElementById('two').value;
        if(one===''||two===''){
            alert('fill all fields');
            return false;
        }
        alert('form done');
        return true;
    }
</script>
</html>
```

### Output:
A form that alerts users if they do not fill in all required fields before submission.

---

## 4. Responsive Navigation Bar

A responsive navigation bar that adapts to different screen sizes.

### Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Nav Bar</title>
    <style>
        *{ padding:0; margin:0; box-sizing: border-box; }
        .navbar{ display: flex; justify-content: space-between; align-items: center; background-color: #2c3e50; color: white; }
        .logo{ font-size: 20px; font-weight: 500; margin: 8px; }
        .navbar-links ul{ display: flex; }
        .navbar-links ul li{ list-style: none; }
        .navbar-links ul li a{ text-decoration: none; color:honeydew; display: block; padding: 18px; }
        .navbar-links ul li a:hover{ background-color: #34495e; }
        .btn{ position: absolute; top:16px; right:16px; width:30px; height: 22px; display:none; flex-direction: column; justify-content: space-between; }
        .bar{ height: 3px; width: 100%; background-color: #fff; }
        @media (max-width:600px) {
            .btn{ display: flex; }
            .navbar-links{ display: none; width: 100%; }
            .navbar{ flex-direction: column; align-items: flex-start; }
            .navbar-links.active{ display:flex; }
        }
    </style>
</head>
<body>
    <div class="navbar">
        <div class="logo">Surya</div>
        <a href="#" class="btn">
            <span class="bar"></span>
            <span class="bar"></span>
            <span class="bar"></span>
        </a>
        <div class="navbar-links">
            <ul>
                <li><a href="#">Home</a></li>
            </ul>
        </div>
    </div>
</body>
</html>
```

---

## Conclusion
These projects demonstrate essential HTML & CSS concepts. Let me know if you want to see more projects!

