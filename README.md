# User instructions:

## Introduction
The calculator.py script provides a menu-driven interface for performing various matrix and scalar operations. Here's a breakdown of what each option does:

### Initial Options
1. **Enter your matrix:** This option prompts the user to input a matrix using the input_matrix function.
2. **Enter your scalar:** This option prompts the user to input a scalar using the input_scalar function.
3. **Exit:** This option ends the program.
### Matrix Operations
1. **Add another Matrix:** This option prompts the user to input another matrix and adds it to the current matrix.
2. **Subtract another Matrix:** This option prompts the user to input another matrix and subtracts it from the current matrix.
3. **Multiply with another Matrix:** This option prompts the user to input another matrix and multiplies it with the current matrix.
4. **Divide by another Matrix:** This option prompts the user to input another matrix and divides the current matrix by it.
5. **Transpose Matrix:** This option transposes the current matrix.
6. **Invert Matrix:** This option inverts the current matrix.
7. **Add Scalar to Matrix:** This option adds the current scalar to the current matrix.
8. **Subtract Scalar from Matrix:** This option subtracts the current scalar from the current matrix.
9. **Multiply by a scalar:** This option multiplies the current matrix by the current scalar.
10. **Divide by a scalar:** This option divides the current matrix by the current scalar.
11. **Clear Results:** This option clears the current matrix.
12. **Show Current Value:** This option displays the current matrix.
13. **Back to Main Menu:** This option returns to the initial options menu.
14. **Exit:** This option ends the program.
### Scalar Operations
1. **Multiply by a matrix:** This option multiplies the current scalar by a matrix input by the user.
2. **Add to a matrix:** This option adds the current scalar to a matrix input by the user.
3. **Subtract from a matrix:** This option subtracts the current scalar from a matrix input by the user.
4. **Clear results:** This option clears the current scalar.
5. **Show current value:** This option displays the current scalar.
6. **Back to main menu:** This option returns to the initial options menu.
7. **Exit:** This option ends the program.

## How to Use
**Inputting a Matrix**

To input a matrix, the script will prompt you with *'Enter matrix rows, separated by ;'*. You should enter each row of your matrix, separated by a semicolon (;). Within each row, separate each element with a comma (,). For example, to input a 2x2 matrix with elements 1, 2, 3, and 4, you would enter 1,2;3,4.

**Inputting a Scalar**

To input a scalar, the script will prompt you with *'Enter a scalar:'*. You should enter a single number.

# Description of matrix functions and how they work

## Addiction
Function **add_matrices** first checkes the validity of the metrices by a function **validate_matrix** that makes sure all rows are the same length and then checkes if the matrices are the same size by using the check_same_dimensions function. After that it returns added matrix by adding every value on the first matrix to its equivalent in the second matrix.

Function **scalar_add** first checkes the validity of the metrices by a function **validate_matrix** that makes sure all rows are the same length and returns new matrix where each element is the sum of the corresponding element in the original matrix and the scalar.
## Subtraction
Function **subtract_matrices** first checkes the validity of the metrices by a function **validate_matrix** that makes sure all rows are the same length and then checkes if the matrices are the same size by using the check_same_dimensions function. After that it returns subctructed matrix by subtrusting every value on the second matrix from its equivalent in the first matrix.

Function **scalar_subtract** first checkes the validity of the metrices by a function **validate_matrix** that makes sure all rows are the same length and returns new matrix where each element is the difference between the corresponding element in the original matrix and the scalar.
## Multiplication
Function **multiply_matrices** first checkes the validity of the metrices by a function **validate_matrix** that makes sure all rows are the same length and then by check_multiplication_compatability function checks if the number of columns in the first matrix is equal to the number of rows in the second matrix. After that it returns a sum of a and b for every pair of two arguments paird by a zip() method for each row of the first matrix and column of the second matrix that multiplies the equvlents of each.

Function **scalar_multiply** first checkes the validity of the metrices by a function **validate_matrix** that makes sure all rows are the same length and returns new matrix where each element is the product of the corresponding element in the original matrix and the scalar.
## Inverse
Function **get_matrix_inverse** first checkes the validity of the metrices by a function **validate_matrix** that makes sure all rows are the same length and then by check_square_matrix funcion checks if the matrix is square. The size of the matrix is then determined, and an identity matrix of the same size is created. The function then creates an augmented matrix, which is essentially the input matrix appended with the identity matrix. The function then enters a loop that performs Gaussian elimination on the augmented matrix. If it encounters a row where all elements in the current column are zero, it raises a ValueError, indicating that the matrix is not invertible. After the Gaussian elimination process is complete, the function returns the right half of the augmented matrix, which is now the inverse of the original matrix.
## Division
Function **divide_matrices** first checkes the validity of the metrices by a function **validate_matrix** that makes sure all rows are the same length and then by the function check_square_matrix checks if the second matrix is square as only square matrices have an inverse. Then by using function get_matrix_inverse it creates an inverse of the second matrix and returns a multiplication of the first matrix and the inverted second matrix.

Function **scalar_divide** first checkes the validity of the metrices by a function **validate_matrix** that makes sure all rows are the same length and returns new matrix here each element is the quotient of the corresponding element in the original matrix and the scalar.
## Transpose
Function **transpose_matrix** first checkes the validity of the metrices by a function **validate_matrix** that makes sure all rows are the same length and then returns a new matrix where the rows and columns are swapped. It achieves this by iterating over the columns of the original matrix and extracting the corresponding elements from each row.

# Description of main calculator program.

## input_matrix function
The **input_matrix** function is designed to take matrix input from the user. The user is expected to enter the matrix rows, separated by semicolons (;), and within each row, the elements are separated by commas (,). The function takes matrix input from the user, validates the input, and returns the matrix. If the input is not valid, it prints an error message.

## input_scalar function
The **input_scalar** function is designed to take scalar input from the user. The user is expected to enter a single number, which represents the scalar. The function takes scalar input from the user, validates the input, and returns the scalar. If the input is not valid, it prints an error message.

## display_matrix function
The **display_matrix** function is designed to display a matrix to the user. The function takes a matrix as an argument and prints it to the console in a formatted manner. If the matrix is empty, it prints 'Empty matrix'. This function provides a way for the user to visually inspect the current state of the matrix.

## main function
The **main** function is the entry point of the **calculator.py** script. It orchestrates the flow of the program and interacts with the user. The function first initializes an empty matrix and a scalar with a value of 0. It then enters a loop where it presents a menu of options to the user and performs the selected operation.

The options include entering a matrix or a scalar, performing various matrix operations (like addition, subtraction, multiplication, division, transposition, and inversion), performing scalar operations (like addition, subtraction, multiplication, and division with a matrix), and displaying or clearing the current matrix or scalar.

The function validates user input and handles errors appropriately, ensuring that the operations are performed on valid matrices and scalars. If the user chooses to exit, the function breaks the loop and the program ends.

In summary, the main function controls the flow of the **calculator.py** script, allowing the user to perform various matrix and scalar operations and managing the current matrix and scalar.

# References of any web sites etc. used.
Sayon, S. (2023). How to print a matrix in Python [3 ways] - Java2Blog. Java2Blog, 6 December 2023. Available from: https://java2blog.com/print-a-matrix-in-python/.


## Project status
If you have run out of energy or time for your project, put a note at the top of the README saying that development has slowed down or stopped completely. Someone may choose to fork your project or volunteer to step in as a maintainer or owner, allowing your project to keep going. You can also make an explicit request for maintainers.
