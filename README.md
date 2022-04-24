# CALCULATOR
HOW TO MAKE A CALCULATOR USING HTML CSS & JAVASCRIPT ?

Welcome to today’s tutorial. In today’s tutorial, we will learn how to create a simple calculator. For this tutorial, we will be using HTML, CSS and Javascript. This is a perfect tutorial for javascript beginners. Let us begin with the tutorial.

![image](https://user-images.githubusercontent.com/60469322/164974001-1bd4b520-4543-4c54-a84a-6c9d7df31dc3.png)

Project Folder Structure:

Let us see what the project folder structure looks like. The project folder is called – Calculator. Inside this folder, we have three files – index.html, style.css and script.js. They are HTML document, stylesheet and script respectively.

HTML:

We start with the HTML code. Copy the code below and paste it into your HTML file.
The HTML code consists of a div with a class calculator. Inside the calculator, we have two main divs. The first is the display div and the second is the buttons div.

The display div consists of an input element with the type text. We set the placeholder to zero.
Inside buttons, we have 18 different buttons. They are numbers from 0 to 9, AC and DEL button, 4 basic operators, an equal to button and a decimal button. For all the buttons except AC, DEL and equal we assign a class called input-button.

<!DOCTYPE html>
<html lang="en">
  <head>
     <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Calculator</title>
    <!-- Google Font -->
    <link
      href="https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@500&display=swap"
      rel="stylesheet"
    />
    <!-- Stylesheet -->
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div class="calculator">
      <div class="display">
        <input type="text" placeholder="0" id="input" disabled />
      </div>
      <div class="buttons">
        <!-- Full Erase -->
        <input type="button" value="AC" id="clear" />
        <!-- Erase Single Value -->
        <input type="button" value="DEL" id="erase" />
        <input type="button" value="/" class="input-button" />
        <input type="button" value="*" class="input-button" />
        <input type="button" value="7" class="input-button" />
        <input type="button" value="8" class="input-button" />
        <input type="button" value="9" class="input-button" />
        <input type="button" value="-" class="input-button" />
        <input type="button" value="6" class="input-button" />
        <input type="button" value="5" class="input-button" />
        <input type="button" value="4" class="input-button" />
        <input type="button" value="+" class="input-button" />
        <input type="button" value="1" class="input-button" />
        <input type="button" value="2" class="input-button" />
        <input type="button" value="3" class="input-button" />
        <input type="button" value="=" id="equal" />
        <input type="button" value="0" class="input-button" />
        <input type="button" value="." class="input-button" />
      </div>
    </div>
    <!-- Script -->
    <script src="script.js"></script>
  </body>
</html>
