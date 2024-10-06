# SparseMatrix Implementation

## Overview

This project provides an implementation of a sparse matrix, a matrix where most of the elements are zeros. The `SparseMatrix` class supports basic matrix operations such as loading matrices from a file, getting and setting elements, and performing matrix addition, subtraction, and multiplication.

---

### Features

- **Sparse Matrix Representation:** Efficiently stores non-zero elements.
- **Matrix Operations:** Supports addition, subtraction, and multiplication of sparse matrices.
- **File I/O:** Can load matrix data from a file and save results to a file.

### Usage

#### 1. Matrix Format

Matrices should be represented in a specific format in the input file:

- The first line indicates the number of rows: `rows=<number_of_rows>`.
- The second line indicates the number of columns: `cols=<number_of_columns>`.
- Each subsequent line represents a non-zero element in the format `(row, col, value)`.

#### 2. Operations Supported

The following operations are supported:

- **Addition** of two matrices.
- **Subtraction** of two matrices.
- **Multiplication** of two matrices (if the dimensions are compatible).

#### 3. Example Input File


This file represents a 3x3 matrix with the following non-zero elements:
- 5 at position (0, 0)
- 8 at position (1, 2)
- 3 at position (2, 1)

#### 4. How to Run

To use the program, run the `main` function, which will guide you through selecting the operation and loading the matrices from files.

1. Clone or download the repository containing the `SparseMatrix` class.
2. Open a terminal and navigate to the directory.
3. Run the script using:

```bash
python sparse_matrix.py
matrix1 = SparseMatrix('matrix1.txt')
matrix2 = SparseMatrix('matrix2.txt')

result = matrix1.add(matrix2)  # Perform addition
result = matrix1.subtract(matrix2)  # Perform subtraction
result = matrix1.multiply(matrix2)  # Perform multiplication

# Save result to a file
with open('result.txt', 'w') as output_file:
    for (row, col), value in result.elements.items():
        output_file.write(f"({row}, {col}, {value})\n")

