<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML & CSS Projects Blog</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }
        .container {
            width: 80%;
            margin: auto;
            background: white;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1, h2 {
            color: #444;
        }
        pre {
            background: #222;
            color: #f4f4f4;
            padding: 10px;
            overflow-x: auto;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>A Collection of HTML & CSS Projects</h1>
        <p>In this blog, I will be showcasing multiple HTML & CSS projects that I have worked on. Each project demonstrates different aspects of web development.</p>
        
        <h2>1. Typing Effect with Search Box</h2>
        <p>This project creates a typing effect for a heading while also including a simple search box.</p>
        <pre>
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;style&gt;
        body { background-color: #1e1e2f; color: white; font-family: 'Courier New'; }
        h1 { animation: typing 3s steps(14) forwards, blink 0.5s infinite; }
        @keyframes typing { from { width: 0 } to { width: 14ch } }
        @keyframes blink { 50% { border-color: transparent } }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h1&gt;Surya Is A Boy&lt;/h1&gt;
    &lt;input type="text" placeholder="Search..."&gt;
&lt;/body&gt;
&lt;/html&gt;
        </pre>
        
        <h2>2. Chessboard Layout</h2>
        <p>This project builds a chessboard layout using HTML & CSS, with chess piece symbols.</p>
        <pre>
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;style&gt;
        body { display: flex; flex-wrap: wrap; width: 800px; height: 800px; }
        .two { width: 100px; height: 100px; text-align: center; font-size: 60px; }
        .three { background-color: black; }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;div class="one"&gt;
        &lt;div class="two"&gt;&#9820;&lt;/div&gt;
        &lt;div class="two three"&gt;&#9822;&lt;/div&gt;
        &lt;div class="two"&gt;&#9821;&lt;/div&gt;
        &lt;div class="two three"&gt;&#9819;&lt;/div&gt;
    &lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
        </pre>
        
        <h2>3. Simple Form Validation</h2>
        <p>A basic form validation script that ensures the user fills in the required fields before submitting.</p>
        <pre>
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;script&gt;
        function formvalid() {
            const name = document.getElementById('one').value;
            if (name === '') {
                alert('Fill all fields');
                return false;
            }
            alert('Form done');
            return true;
        }
    &lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;form onsubmit="return formvalid()"&gt;
        NAME: &lt;input type="text" id="one"&gt;
        &lt;input type="submit"&gt;
    &lt;/form&gt;
&lt;/body&gt;
&lt;/html&gt;
        </pre>
        
        <h2>4. Responsive Navigation Bar</h2>
        <p>A responsive navigation bar that adapts to different screen sizes.</p>
        <pre>
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;style&gt;
        .navbar { display: flex; background-color: #2c3e50; color: white; }
        .navbar-links ul { display: flex; }
        @media (max-width: 600px) {
            .navbar-links { display: none; }
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;div class="navbar"&gt;
        &lt;div class="logo"&gt;Surya&lt;/div&gt;
        &lt;div class="navbar-links"&gt;
            &lt;ul&gt;
                &lt;li&gt;&lt;a href="#"&gt;Home&lt;/a&gt;&lt;/li&gt;
            &lt;/ul&gt;
        &lt;/div&gt;
    &lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
        </pre>
        
        <h2>Conclusion</h2>
        <p>These projects demonstrate essential HTML & CSS concepts. Let me know if you want to see more projects!</p>
    </div>
</body>
</html>
