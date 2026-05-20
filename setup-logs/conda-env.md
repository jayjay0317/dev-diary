# Troubleshooting: Setting up PyTorch Environment

## 1. Goal
To set up a stable PyTorch development environment with GPU acceleration in a local Jupyter Notebook.

## 2. Issue
Faced `ModuleNotFoundError` when importing torch after creating a new conda environment.

## 3. Solution
1. **Create environment:** `conda create -n pytorch-env python=3.10`
2. **Install dependencies:** `conda install ipykernel`
3. **Register kernel:** `python -m ipykernel install --user --name pytorch-env --display-name "Python (PyTorch)"`

## 4. Key Takeaways
- Always distinguish between the `(base)` terminal and the `(pytorch-env)` terminal.
- Ensure Jupyter Notebook is installed within the specific environment.

## 5. References
- [Official PyTorch Installation Guide](https://pytorch.org/)
