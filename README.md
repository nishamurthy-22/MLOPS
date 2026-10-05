# MLOPS

Lab 1: Python virtual environment, tests with pytest and unittest, and CI with GitHub Actions.

## What I changed from the original lab

- Added four new functions to the calculator: division (fun5), power (fun6), modulus (fun7) and average (fun8). Division and modulus also check for divide by zero.
- Wrote two tests for every function in both pytest and unittest, so there are 16 tests in each file. I added tests for invalid inputs and divide by zero cases too.
- Updated the GitHub Actions workflows to newer versions (checkout@v4, setup-python@v5, upload-artifact@v4) and Python 3.11.
