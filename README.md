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


CSS:

Now let us stylesheet this calculator using CSS. Copy the code provided below and paste it into your stylesheet.

We start by discarding unwanted margins and paddings from all the elements. We set the background of the body to a linear gradient with solid colour stops.
Next, we set the width of the calculator to 400px and centre it using transforms. We even add some box shadows to make it stand out. To make it look even sleeker, we add some paddings to it.

In the next step, we set the width of the display and input element to 100%. We also use right as a value from the text-align property. We use the grid layout to position and arrange the buttons. You can further customize the buttons and display to suit your style.

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: "Roboto Mono", monospace;
}
body {
  height: 100vh;
  background: linear-gradient(to bottom, #f9544c 50%, #090c31 50%);
}
.calculator {
  width: 400px;
  background-color: #15173c;
  padding: 50px 30px;
  position: absolute;
  transform: translate(-50%, -50%);
  top: 50%;
  left: 50%;
  border-radius: 8px;
  box-shadow: 0 20px 50px rgba(0, 5, 24, 0.4);
}
.display {
  width: 100%;
}
.display input {
  width: 100%;
  padding: 15px 10px;
  text-align: right;
  border: none;
  background-color: transparent;
  color: #ffffff;
  font-size: 35px;
}
.display input::placeholder {
  color: #9490ac;
}
.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 20px;
  margin-top: 40px;
}
.buttons input[type="button"] {
  font-size: 20px;
  padding: 17px;
  border: none;
  background-color: transparent;
  color: #ffffff;
  cursor: pointer;
  border-radius: 5px;
}
.buttons input[type="button"]:hover {
  box-shadow: 0 8px 25px #000d2e;
}
input[type="button"]#equal {
  grid-row: span 2;
  background-color: #f9544c;
}
input[type="button"][value="0"] {
  grid-column: span 2;
}

Javascript:

Now to add functionality to the calculator we will be using javascript. Copy the code below and paste it into your javascript file.

I have already added explanatory comments to the code for understanding so I won’t be explaining the Javascript code in detail.


We start by creating a variable called equal_pressed which is set to zero. Every time the equal to the button is pressed, the value of the equal_pressed variable is changed to one.

So once any evaluation is completed and equal to the button is pressed, the display will clear itself when the user enters a new number or operator for evaluation.

We add a click event listener to the clear button. When AC is pressed the whole display is cleared. Similar to this, we add a click event listener to erase button. Here we use the substr method to delete/remove the last entered digit from the display.

let equal_pressed = 0;
//Refer all buttons excluding AC and DEL
let button_input = document.querySelectorAll(".input-button");
//Refer input,equal,clear and erase
let input = document.getElementById("input");
let equal = document.getElementById("equal");
let clear = document.getElementById("clear");
let erase = document.getElementById("erase");
window.onload = () => {
  input.value = "";
};
//Access each class using forEach
button_input.forEach((button_class) => {
  button_class.addEventListener("click", () => {
    if (equal_pressed == 1) {
      input.value = "";
      equal_pressed = 0;
    }
    //display value of each button
    input.value += button_class.value;
  });
});
//Solve the user's input when clicked on equal sign
equal.addEventListener("click", () => {
  equal_pressed = 1;
  let inp_val = input.value;
  try {
    //evaluate user's input
    let solution = eval(inp_val);
    //True for natural numbers
    //false for decimals
    if (Number.isInteger(solution)) {
      input.value = solution;
    } else {
      input.value = solution.toFixed(2);
    }
  } catch (err) {
    //If user has entered invalid input
    alert("Invalid Input");
  }
});
//Clear Whole Input
clear.addEventListener("click", () => {
  input.value = "";
});
//Erase Single Digit
erase.addEventListener("click", () => {
  input.value = input.value.substr(0, input.value.length - 1);
});

That’s it.Your & MY calculator is now ready. Incase you have any issues while coding this, you can also tweet. Also, do drop your suggestions and feedback in the comments below.

