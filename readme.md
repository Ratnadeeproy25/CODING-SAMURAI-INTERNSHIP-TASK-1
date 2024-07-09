### README

# Calculator Application

This project is a simple web-based calculator developed using HTML, CSS, and JavaScript. It features basic arithmetic operations and error handling to manage scenarios such as division by zero and invalid inputs. The application is designed to be responsive, ensuring a good user experience across various devices including desktops, tablets, and smartphones.

## Table of Contents

1. [Features](#features)
2. [Technologies Used](#technologies-used)
3. [File Structure](#file-structure)
4. [Functions](#functions)
5. [Lessons Learned](#lessons-learned)
6. [Usage](#usage)
7. [Screenshots](#screenshots)

## Features

- Basic arithmetic operations: Addition, Subtraction, Multiplication, Division, and Modulus.
- Error handling for invalid inputs and division by zero.
- Responsive design for optimal viewing on various screen sizes.
- Clear and delete functionalities for easy input management.

## Technologies Used

- HTML
- CSS
- JavaScript

## File Structure

```
project/
│
├── index.html
├── style.css
└── script.js
```

## Functions

### HTML (index.html)

The HTML file contains the structure of the calculator. It includes:

- A container div for centering the calculator.
- An input field to display the input and result.
- Buttons for digits, operators, and functionalities (AC, DEL, =).

### CSS (style.css)

The CSS file styles the calculator. Key styles include:

- General styling and layout using Flexbox for centering.
- Button styling including size, color, and shadows.
- Media queries to ensure responsiveness on smaller screens.

### JavaScript (script.js)

The JavaScript file handles the functionality of the calculator. Key functions include:

1. **Event Listener for Buttons**:
    ```javascript
    arr.forEach(button => {
        button.addEventListener('click', (e) => {
            // Handling button clicks
        })
    });
    ```
    This function adds event listeners to all buttons, allowing them to interact with the input field.

2. **Evaluation Function**:
    ```javascript
    if (e.target.innerHTML == '=') {
        if (string.includes('/0')) {
            throw new Error('Division by Zero');
        }
        string = eval(string);
        input.value = string;
    }
    ```
    This function evaluates the mathematical expression entered by the user. It includes error handling for division by zero.

3. **Clear and Delete Functions**:
    ```javascript
    else if (e.target.innerHTML == 'AC') {
        string = "";
        input.value = string;
    } else if (e.target.innerHTML == 'DEL') {
        string = string.substring(0, string.length - 1);
        input.value = string;
    }
    ```
    These functions handle the clear (AC) and delete (DEL) functionalities, allowing users to manage their input.

4. **Error Handling**:
    ```javascript
    catch (error) {
        input.value = "Error";
        string = "";
        setTimeout(() => {
            input.value = "";
        }, 2000);
    }
    ```
    This function catches errors, displays an error message, and resets the input after a short delay.

## Lessons Learned

From this project, I have learned:

1. **Basic HTML Structure**:
    - How to structure an HTML document with input fields and buttons.

2. **Styling with CSS**:
    - Applying Flexbox for centering elements.
    - Using media queries to create responsive designs.
    - Styling buttons and input fields for a better user interface.

3. **JavaScript for Interactivity**:
    - Adding event listeners to buttons.
    - Evaluating mathematical expressions using `eval()`.
    - Implementing error handling for invalid inputs.
    - Manipulating the DOM to update the input field.

## Usage

To use the calculator:

1. Open the `index.html` file in a web browser.
2. Use the buttons to input numbers and operators.
3. Click `=` to evaluate the expression.
4. Use `AC` to clear the input and `DEL` to delete the last character.
