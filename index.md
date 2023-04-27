<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Interactive Page</title>
    <style>
      body {
        font-family: Arial, sans-serif;
        background-color: #f2f2f2;
      }
      h1 {
        font-size: 3em;
        color: #555;
        text-align: center;
        margin-top: 50px;
      }
      #wrapper {
        display: flex;
        justify-content: center;
        margin-top: 50px;
      }
      #left {
        flex: 1;
        padding: 20px;
        background-color: #fff;
        box-shadow: 0 0 10px #ccc;
      }
      #right {
        flex: 1;
        padding: 20px;
        background-color: #fff;
        box-shadow: 0 0 10px #ccc;
        margin-left: 20px;
      }
      #button {
        display: block;
        margin: 50px auto;
        padding: 10px 20px;
        font-size: 1.2em;
        background-color: #555;
        color: #fff;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        transition: all 0.3s ease;
      }
      #button:hover {
        background-color: #333;
      }
    </style>
  </head>
  <body>
    <h1>Interactive Page</h1>
    <div id="wrapper">
      <div id="left">
        <h2>Left Panel</h2>
        <p>Enter your name:</p>
        <input type="text" id="name">
        <button onclick="sayHello()">Say Hello</button>
        <div id="output"></div>
      </div>
      <div id="right">
        <h2>Right Panel</h2>
        <p>Select a color:</p>
        <input type="radio" name="color" id="red" value="red">
        <label for="red">Red</label><br>
        <input type="radio" name="color" id="green" value="green">
        <label for="green">Green</label><br>
        <input type="radio" name="color" id="blue" value="blue">
        <label for="blue">Blue</label><br>
        <button onclick="changeColor()">Change Color</button>
      </div>
    </div>
    <button id="button" onclick="toggleVisibility()">Toggle Visibility</button>
    <script>
      function sayHello() {
        var name = document.getElementById("name").value;
        var output = document.getElementById("output");
        output.innerHTML = "Hello, " + name + "!";
      }
      function changeColor() {
        var color = document.querySelector('input[name="color"]:checked').value;
        document.body.style.backgroundColor = color;
      }
      function toggleVisibility() {
        var wrapper = document.getElementById("wrapper");
        if (wrapper.style.display === "none") {
          wrapper.style.display = "flex";
        } else {
          wrapper.style.display = "none";
        }
      }
    </script>
  </body>
</html>
