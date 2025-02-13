# Linear Equation Maths Game Documentation

## Introduction

The Linear Equation Maths Game is a mock exam style interactive game where users can practice linear algebra by solving simple randomly generated linear equestions. Players must answer a total of 10 questions by working out the value of the 'Y' variable and submitting their answers using the games graphical user interface.


## User Guide

Are you looking to improve your basic linear alebra maths skills? Well this game is right for you! Test your skill level by attempting to solve 10 randomly generated linear equations and you aren't happy with your score, then start a new game and try again!


### Features
- **Avoid memorisation with randomly generated linear equations**: Equations consist of two whole numbers, each from the value of 1 to 10, summed, subracted or multiplied together with an answer after an equals sign. One number is hidden under the variable 'Y'. This is the value that you must work out.
- **Learn and improve as you play with instant feedback on your answers**: Receive your mark after you answer each question. If your answer was incorrect, the game will tell you what the correct answer was. 
- **Sudden emergency? Easy to quit whenever you want**: Just press the 'Quit' button to end the game at any time.
- **Not so good with numbers? Keeps track of your score and your progress**: Your score and the amount of questions answered will be displayed throughout.  
- **Scared of the terminal? Play using the games simple user interface**: Do you miss Windows XP? Enjoy the games simple but effective user interface design. Who needs flashy colours and animations, right?
- **Cat like's walking on your keyboard? Invalid answers will not be accepted**: If you accidentally submit a blank value or a word instead of anumber, your answer will not be accepted and you will quietly be prompted for a valid answer. No one will ever know.


### What you'll need

- Required: Python (version 3.9 or later) installed on your computer.
- Optional: A Python interpreter or IDE such as PyCharm or Visual Studio Code with Python extension installed.

### How to Launch
- Simply run the game in your terminal or open the 'main.py' file with Python.

### How to Play
1. Read the instructions and click 'Start Game'.
2. Solve the equation.
3. Input your answer with your keyboard.
4. Click submit.
5. Answer 10 questions to complete the game.

### Step by step example:
![image of Instructions Page Guide](https://github.com/4lex-cooper/LinEqMathGame/blob/main/Instructions%20Page%20Guide.png)
![image of Questions Page Guide](https://github.com/4lex-cooper/LinEqMathGame/blob/main/Questions%20Page%20Guide.png)
![image of Game Completed Page Guide](https://github.com/4lex-cooper/LinEqMathGame/blob/main/Game%20Completed%20Page%20Guide.png)


## Technical Documentation

### To clone the repository:

```bash
git clone https://github.com/4lex-cooper/LinEQMathGame.git
```


### Code Overview

**main.py**

This is the main game file. It contains all the GUI interactions.

The code follows an object-oriented programming approach to enable more tidy and organised code as well as enabling an easier way for variables, GUI elements and widgets to be altered within methods that are outside of those where they were originally created. By attaching variables as attributes of the class with the 'self' parameter and by handling inheritance with the super() function we can access and alter these variables from within different methods.

The parent class AppWindow represents the main tkinter GUI window and contains the Start Game button widget.

The child classes InstructionsFrame and QuestionsFrame represent tkinter frames that contain the initial instructions page, and the main questions page plus the final game completion screen, respectively.

All classes contain an '\_\_init__' method which sets the classes initialised state. 

Methods with '_click' at the end of their name are executed first when the user clicks on a button in the GUI. These methods are attached to their corresponding button widgets by using the tkinter method '.configure(command=)' on the widget instance objects. 

Example:

```python
self.close_button = ttk.Button(self, text="Close", command=self.close_click)
```

**functions.py**

Contains re-usable pure functions (if we ignore the argument that generate_lineq_question() is not a pure function as it uses the random module) that improve the readability of the main game file. All have docstrings to exaplain their purpose, any arguments and data that is returned by the function.


**functions_test.py**

This test file contains unit tests designed to ensure that the main functions within functions.py return valid results. To run tests, Pytest must be installed and called within the terminal.


### Python Modules Used

- random: Used in the function generate_lineq_question() to generate random numbers and choose a random operator.
- tkinter: Used in main.py to create the games GUI (Graphical User Interface).
- tkk: Used to create styled widgets within the GUI.


### Python Version

Python version 3.12.7 was used to develop this application.

### Coding standards

All code follows the PEP8 style guide.


### Variables

| Variable Name     | Data Type | Description                                              |
| ----------------- | --------- | -------------------------------------------------------- |
| instructions      | string    | Text that describes how to play the game for the user |
| question          | string    | Current linear equation maths question |
| user_answer_text  | string    | Latest answer submitted by the user |
| user_answer       | integer   | Latest answer submitted by the user converted to the int data type |
| correct_answer    | integer   | Correct answer to the current question |
| score             | integer   | Number of correct answers the user has submitted in the current game |
| questions_answered | integer  | Number of questions the user has answered in the current game |
| total_questions   | integer   | Total number of questions to be answered to complete the game |





