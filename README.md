# Anaconda Setup and Usage in VS Code

This guide will help you install **Anaconda**, create a Python environment, and use it in **Visual Studio Code (VS Code)**.

## 1. Install Anaconda

1. Go to the [Anaconda Downloads page](https://www.anaconda.com/products/distribution) and download the installer for your OS (Windows, macOS, Linux).
2. Run the installer:
   - **Windows:** Follow the wizard. Optional: check “Add Anaconda to my PATH environment variable.”
   - **macOS/Linux:** Follow the terminal instructions.
3. Verify installation by running:

```bash
conda --version
```

## 2. Create a Conda Environment

```bash
conda create --name myenv python=3.11
```

- Replace `myenv` with your environment name.
- Replace `3.11` with the Python version you want.

## 3. Activate / Deactivate the Environment

Activate:

```bash
conda activate myenv
```

Deactivate:

```bash
conda deactivate
```

## 4. Install Packages (Optional)

Using Conda:

```bash
conda install package_name
conda install pandas
```

Using Pip:

```bash
pip install package_name
pip install pyclustering
```

## 5. Using Anaconda Environment in VS Code

### Step 1: Install Extensions

1. Open VS Code.
2. Go to **Extensions** (`Ctrl+Shift+X` or `Cmd+Shift+X`).
3. Install:
   - **Python** (Microsoft)
   - **Jupyter**

### Step 2: Select Python Interpreter

1. Open the command palette (`Ctrl+Shift+P` or `Cmd+Shift+P`).
2. Search `Python: Select Interpreter`.
3. Choose your Anaconda environment (`myenv`).

### Step 3: Use Jupyter Notebook / Kernel

1. Open a `.ipynb` notebook.
2. Click **Kernel** (top-right corner).
3. Select your environment (`myenv`).

## 6. Verify Environment in VS Code

```python
import sys
print(sys.executable)
```

It should point to your Anaconda environment.

## 7. Tips

- Always activate your environment before installing packages.
- Keep environments isolated to avoid conflicts.
- Update Conda regularly:

```bash
conda update conda
```

You are now ready to efficiently use Anaconda environments in VS Code!

