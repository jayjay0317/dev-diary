# Troubleshooting: Setting up PyTorch Environment

## 1. Goal
To set up a stable PyTorch development environment with GPU acceleration in a local Jupyter Notebook.

## 2. Issue
Initially tried to run `jupyter notebook` in the `(base)` environment. Encountered `ModuleNotFoundError: No module named 'torch'` because PyTorch was not installed in the global base environment.

## 3. Solution
1. **Create environment:** `conda create -n pytorch-env python=3.10`
2. **Install dependencies:** `conda install pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia`
3. **Install Jupyter & kernel tool:** `conda install ipykernel`
4. **Register kernel:** `python -m ipykernel install --user --name pytorch-env --display-name "Python (PyTorch)"`

## 4. Key Takeaways
- Always distinguish between the `(base)` terminal and the `(pytorch-env)` terminal.
- Avoid installing project-specific libraries in the `(base)` environment to maintain system stability.
- Ensure Jupyter Notebook and necessary kernels are installed within the project's specific virtual environment.
