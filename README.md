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




CSS:

Now let us stylesheet this calculator using CSS. Copy the code provided below and paste it into your stylesheet.

We start by discarding unwanted margins and paddings from all the elements. We set the background of the body to a linear gradient with solid colour stops.
Next, we set the width of the calculator to 400px and centre it using transforms. We even add some box shadows to make it stand out. To make it look even sleeker, we add some paddings to it.

In the next step, we set the width of the display and input element to 100%. We also use right as a value from the text-align property. We use the grid layout to position and arrange the buttons. You can further customize the buttons and display to suit your style.


Javascript:

Now to add functionality to the calculator we will be using javascript. Copy the code below and paste it into your javascript file.

I have already added explanatory comments to the code for understanding so I won’t be explaining the Javascript code in detail.


We start by creating a variable called equal_pressed which is set to zero. Every time the equal to the button is pressed, the value of the equal_pressed variable is changed to one.

So once any evaluation is completed and equal to the button is pressed, the display will clear itself when the user enters a new number or operator for evaluation.

We add a click event listener to the clear button. When AC is pressed the whole display is cleared. Similar to this, we add a click event listener to erase button. Here we use the substr method to delete/remove the last entered digit from the display.



That’s it.Your & MY calculator is now ready. Incase you have any issues while coding this, you can also tweet. Also, do drop your suggestions and feedback in the comments below.

