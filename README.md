# Elementalist: Master of Atoms (MoA)

## Description

A program that takes a name of an element as input and outputs it's amount of subatomic particles and it's four different quantum numbers. This project aims to provide a useful tool for students and maybe even professionals in chemistry to quickly retrieve detailed information about the atomic structure of elements. Additionaly, this program has an option for a quiz/trivia, allowing the user to test their skills and what they have learned from the program itself.

## Features

* Calculates subatomic particles (protons, neutrons, electrons) for the given element
* Calculates the given element's four quantum numbers (n, l, ml, ms) for each element
* User friendly interface for inputting element names and displaying results
* Input validation to ensure accurate and reliable results

  ## Summarized pseudocode of program
```
MAIN MENU
DISPLAY "Welcome to Elemental Analyzer!"
DISPLAY "1. Retrieve element information"
DISPLAY "2. Play quiz/trivia mode"
DISPLAY "3. Exit"

DISPLAY ""

DISPLAY "Choose an option: "
INPUT user_choice

IF user_choice == 1 THEN
  DISPLAY "Enter element name: "
  INPUT element_name
  VALIDATE element_name
    IF valid THEN
      RETRIEVE element_data
      CALCULATE subatomic_particles AND quantum_numbers
      DISPLAY subatomic_particles AND quantum_numbers
    ELSE
      DISPLAY "Invalid element name"
    END IF

ELSE IF user_choice == 2 THEN
  QUIZ MODE
  GENERATE random questions about elements
  DISPLAY question
  INPUT user_answer
  CHECK answer
    IF correct THEN
      DISPLAY "Correct!"
    ELSE
      DISPLAY "Incorrect. The correct answer is __"
    END IF
      REPEAT until user chooses to exit

ELSE IF user_choice == 3 THEN
  EXIT PROGRAM
ELSE
  DISPLAY "Invalid choice. Please choose again."
  REPEAT MAIN MENU (LOOP)
  ```
