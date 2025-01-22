# CS5720: Neural Networks and Deep Learning
## In-Class Programming Assignment 2

**Student Name:** Nidhin Ninan  
**Student ID:** [Your Student ID]  
**Course:** CS5720 Neural Networks and Deep Learning (Spring 2025)  
**University:** University of Central Missouri

## Description
This repository contains the solutions for In-Class Programming Assignment 2. The assignment consists of two problems focused on Python classes and NumPy array operations.

### Problem 1: Employee Class Inheritance
File: `Week2_NN_1.ipynb`

Implementation of two classes demonstrating inheritance and class methods:

1. Base Class (`Employee`):
   - Class variables to track total number of employees and salary sum
   - Constructor initializes employee details (name, family, salary, department)
   - Class methods to:
     - Count total number of employees
     - Calculate average salary across all employees

2. Derived Class (`Fulltime_Employee`):
   - Inherits from `Employee` class
   - Uses super() to initialize parent class attributes
   - Demonstrates inheritance by maintaining the same salary and employee counting functionality

The code demonstrates:
- Class inheritance
- Class variable usage for tracking aggregate data
- Class method implementation
- Super() constructor usage
- Instance creation and method calling

### Problem 2: NumPy Array Operations
File: `Week2_NN_2.ipynb`

Implementation of various NumPy array operations:

1. Vector Creation:
   - Creates a 1D array of size 20 with random float values
   - Uses np.random.uniform() to generate numbers between 1 and 20
   - Rounds values to 2 decimal places using np.round()

2. Array Reshaping:
   - Transforms the 1D array (20 elements) into a 2D array (4x5)
   - Uses np.reshape() for dimensional transformation

3. Maximum Value Replacement:
   - Identifies maximum value in each row using np.argmax()
   - Replaces maximum values with 1 using array indexing
   - Implements solution without using loops
   - Uses numpy's broadcasting capabilities for efficient operation

## Note
- Make sure to initialize/create you conda environment appropriately with the required packages like Jupyterlab, jupyterlab-server and numpy with you use a jupyterlab project in PyCharm.
- Add the conda environemnt to PyCharm by adding a Sytem Interpreter and then select the environment in the Jupyterlab project that we work with
