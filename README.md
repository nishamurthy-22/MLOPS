# MLOPS

Lab 1: Python virtual environment, tests with pytest and unittest, and CI with GitHub Actions.

## Project structure
- `src/calculator.py` - calculator functions
- `test/test_pytest.py` - tests written with pytest
- `test/test_unittest.py` - tests written with unittest
- `.github/workflows/` - GitHub Actions workflows that run the tests on every push to main
- `data/` - placeholder folder for data files

## How to run locally

    python3 -m venv lab_01
    source lab_01/bin/activate
    pip install -r requirements.txt
    python3 -m pytest test/test_pytest.py --cov=src --cov-report=term
    python3 -m unittest test.test_unittest -v

## What I changed from the original lab
- Added four new functions to the calculator: division (fun5), power (fun6), modulus (fun7) and average (fun8). Division and modulus also check for divide by zero.
- Wrote two tests for every function in both pytest and unittest, so there are 16 tests in each file. I added tests for invalid inputs and divide by zero cases too.
- Added code coverage to the CI pipeline using pytest-cov. Each run shows the coverage in the logs and uploads a coverage report as an artifact.
- Updated the GitHub Actions workflows to newer versions (checkout@v4, setup-python@v5, upload-artifact@v4) and Python 3.11.
