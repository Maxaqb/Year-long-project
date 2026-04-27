# Elementalist: Master of Atoms (MoA)

## Description
Elementalist: Master of Atoms (EMoA) is an educational program designed to help students learn about the periodic table in an interactive way. Users can input atomic numbers (1–118) to retrieve detailed information about elements, including their name, symbol, atomic mass, charge, and subatomic particles. The program also features a quiz mode to test knowledge and an instructions section to guide new users.

## Features
- Element Lookup: Retrieve element details by entering an atomic number.  
- Subatomic Calculation: Automatically calculates neutrons based on atomic mass and protons.  
- Interactive Menu: Navigate between Lookup, Quiz, Instructions, and Exit options.  
- Input Validation: Handles invalid inputs gracefully with error messages.  
- Instructional Guide: Explains program purpose and usage for first-time users.  
- Quiz Mode: Randomized questions from a JSON dataset to test chemistry knowledge. 


## Logic Plan / Summarized pseudocode of program

    BEGIN PROGRAM

    IMPORT periodicTable
    IMPORT time
    IMPORT json

    FUNCTION element_lookup:
       DISPLAY "----- Element Lookup -----"
       LOOP FOREVER:
         TRY:
             PROMPT user for atomic number
             IF atomic number is between 1 and 118:
                GET element from periodicTable
                DISPLAY "Element Name: ", element.name
                DISPLAY "Symbol: ", element.symbol
                DISPLAY "Atomic Mass: ", element.mass
                DISPLAY "Charge: ", element.charge
                DISPLAY "Protons: ", element.protons
                DISPLAY "Electrons: ", element.protons
                CALCULATE average neutrons = element.mass - element.protons
                DISPLAY "Neutrons: ", average neutrons
                BREAK LOOP
            ELSE:
                DISPLAY "Invalid atomic number (1–118)"
        EXCEPT ValueError:
            DISPLAY "Invalid input. Please enter a number"

    FUNCTION quiz:
       DISPLAY "----- Quiz Mode -----"
       LOAD quiz-data.json
       RANDOMLY select a question from dataset
       DISPLAY question text
       PROMPT user for answer
       IF user_answer == correct_answer:
          DISPLAY "Correct!"
       ELSE:
          DISPLAY "Incorrect. Correct answer is: ", correct_answer
       RETURN to main menu

    FUNCTION instructions:
       DISPLAY "----- Instructions -----"
       DISPLAY "This program helps you learn chemistry concepts."
       DISPLAY "Menu Options:"
       DISPLAY "1 - Lookup: Enter an atomic number to see element details."
       DISPLAY "2 - Quiz: Answer chemistry questions to test your knowledge."
        DISPLAY "3 - Instructions: Learn how to use the program."
       DISPLAY "4 - Exit: Close the program."

    MAIN PROGRAM LOOP:
       LOOP FOREVER:
           DISPLAY "WELCOME TO OUR EDUCATIONAL GAME!!!"
           DISPLAY "Main Menu Options:"
           DISPLAY "1 - View Periodic Table and Lookup Element"
           DISPLAY "2 - Quiz"
           DISPLAY "3 - Instructions"
           DISPLAY "4 - Exit Game"

        TRY:
            PROMPT user for choice (1–4)

            IF choice == 1:
                DISPLAY asciiArt of periodic table
                CALL element_lookup

            ELSE IF choice == 2:
                CALL quiz

            ELSE IF choice == 3:
                CALL instructions

            ELSE IF choice == 4:
                DISPLAY "Thanks for playing! Goodbye."
                BREAK LOOP

            ELSE:
                DISPLAY "Retry. Please enter 1–4."

        EXCEPT ValueError:
            DISPLAY "Invalid menu choice. Please enter 1, 2, 3, or 4"

    END PROGRAM
