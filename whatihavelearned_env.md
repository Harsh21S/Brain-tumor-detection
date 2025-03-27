# Summary of Learnings

## 1. Conda Environment Management
- **Activating Conda Environment**: You learned how to activate a specific conda environment (e.g., `MRI`) to work within it:
    ```bash
    conda activate MRI
    ```
- **Python Interpreter Issues**: You encountered a problem where a different Python interpreter (`Python313`) was being used instead of the one from your conda environment, leading to issues with package installations not being recognized.

## 2. Correcting Python Interpreter
- **Checking Python Path**: You learned how to check which Python interpreter is in use:
    ```bash
    which python  # On Linux/macOS
    where python  # On Windows
    ```
- **Fixing Interpreter in VS Code**: In VS Code, you can ensure the correct interpreter is being used:
    1. Press `Ctrl+Shift+P` (or `Cmd+Shift+P` on macOS).
    2. Type `Python: Select Interpreter` and choose the one from your conda environment (`MRI`).

## 3. Package Installation in Conda Environment
- **Correct Package Installation**: You learned how to install Python packages inside the conda environment:
    ```bash
    conda install scikit-learn  # Correct way to install sklearn via conda
    ```
- You also learned that using `pip install sklearn` installs an obsolete or incorrect package. Instead, you should install `scikit-learn`:
    ```bash
    %pip install scikit-learn
    ```

## 4. Running Python Files in Conda Environment
- **.ipynb vs .py Files**: Both `.ipynb` (Jupyter Notebook files) and `.py` (Python script files) can be run in a conda environment, but it's crucial that the right Python interpreter is being used in both cases.
- **Running Python Scripts**: To run a Python script (`.py`) in your conda environment:
    ```bash
    python script_name.py
    ```
- Running the script outside the conda environment will lead to missing module errors, as happened with `sklearn`.

## 5. Summary of Errors Encountered
- **ModuleNotFoundError for sklearn**: This error occurred when the environment did not have the correct packages installed or when the wrong Python interpreter was being used.
- **Package Names**: You learned the difference between `sklearn` and `scikit-learn`, which caused confusion.

## Conclusion
- You now understand how to:
    - Properly use and activate conda environments.
    - Manage the correct Python interpreter in your environment.
    - Install packages correctly.
    - Run Jupyter notebooks and Python scripts in conda environments.
    