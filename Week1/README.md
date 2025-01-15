# Neural Networks and Deep Learning - ICP-1

## Problem 1: Full Name and Alternate Characters (Week1_NN_1.ipynb)

### Problem Statement
Write a program that takes two strings (first_name, last_name) from the user and creates a full name. Then create a function that returns every other character in the full name string.

### Implementation Logic
1. Created two functions:
   - `fullname(first, last)`: Combines first and last name with a space between them
   - `string_alternative(full_name)`: Returns every other character using string slicing `[::2]`
2. User inputs first and last name interactively
3. Program prints both the full name and the string with alternate characters

## Problem 2: Word Count in File (Week1_NN_2.ipynb)

### Problem Statement
Write a Python program to find the word count in a file (input.txt) for each line and store the output in output.txt file.

### Implementation Logic
1. Defined file paths for input and output text files
2. Created a dictionary to store word counts
3. Processing steps:
   - Read input file line by line
   - Strip newline characters and print each line
   - Split lines into words and convert to lowercase
   - Count word occurrences using dictionary
4. Print word counts with capitalized words
5. Save results to output file:
   - Original input text
   - Word count for each unique word

## Problem 3: Height Conversion (Week1_NN_3.ipynb)

### Problem Statement
Write a program that reads heights in inches from users into a list and converts these heights to centimeters using list comprehension.

### Implementation Logic
1. Interactive input:
   - Created empty list for heights in inches
   - Used while loop to continuously accept height inputs
   - Loop breaks when user enters 'q'
   ```diff
   - **NOTE: Enter ONLY the correct values as this code as no check to ensure if the entered values are numerical or even logical** 
3. Conversion implementation:
   - Used list comprehension to convert inches to centimeters
   - Formula: height * 2.54
   - Results rounded to 2 decimal places
4. Print both original heights in inches and converted heights in centimeters

## Note
The code follows the rubric guidelines and includes proper documentation. Each implementation includes interactive elements and demonstrates different Python concepts like:
- Function definitions and calls
- String manipulation
- File I/O operations
- List comprehension
- Dictionary operations
- User input handling
- Type conversion
- Formatted output
