# Elementalist: Master of Atoms (MoA)

## Description
Elementalist: Master of Atoms (EMoA) is an educational game that helps students learn about the periodic table. Users can select an atomic number (1–118) to instantly view facts about that element, such as its name, symbol, and the number of particles (protons, electrons, and neutrons) inside its atoms. The program features a simple menu that allows users to look up elements, or view instructions..

## Features
Element Lookup: Retrieves detailed data for any element (atomic number 1–118).

Subatomic Calculation: Automatically calculates the number of protons, electrons, and the average number of neutrons.

Input Validation: Robust error handling ensures the program stays stable even with incorrect inputs.

Interactive Menu: A user-friendly, loop-based interface that allows users to explore features or exit the program gracefully.

Instructional Guide: Built-in guidance on how to navigate the program and understand its purpose.

## Logic Plan / Summarized pseudocode of program

    IMPORT periodictable, time, json

    FUNCTION element_lookup:
    DISPLAY "-----Element Lookup-----"
    LOOP FOREVER:
        TRY:
            PROMPT user for atomic number
            IF atomic number is between 1 and 118:
                GET element from periodictable
                DISPLAY name, symbol, mass, charge, protons, electrons
                CALCULATE average neutrons = mass - protons
                DISPLAY average neutrons
                BREAK LOOP
            ELSE:
                DISPLAY "Invalid atomic number (1-118)"
        EXCEPT ValueError:
            DISPLAY "Invalid input. Please enter a number"

	MAIN PROGRAM LOOP:
    	LOOP FOREVER:
        	DISPLAY Main Menu options (1-4)
        	TRY:
            	PROMPT user for choice
            	IF choice == 1:
                	DISPLAY asciiArt
                	CALL element_lookup
            	ELSE IF choice == 2:
                	DISPLAY "Quiz test under construction"
            	ELSE IF choice == 3:
                	DISPLAY instructions and game purpose
            	ELSE IF choice == 4:
                	DISPLAY "Thanks for playing! Goodbye."
                	BREAK LOOP
            	ELSE:
                	DISPLAY "Retry"
        	EXCEPT ValueError:
            	DISPLAY "Invalid menu choice"
