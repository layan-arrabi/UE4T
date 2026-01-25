# SageMath in GitHub Codespaces

## Installation Complete ✓

SageMath has been installed via conda in your GitHub Codespace and is ready to use!

## How to Use SageMath in Jupyter Notebooks

### Option 1: Change Kernel in Existing Notebook

1. Open your notebook in VS Code (e.g., "New UETn Generator.ipynb")
2. Click on the kernel selector in the top-right corner (it shows "Python 3.x.x")
3. Select **"SageMath"** from the kernel list
4. Your notebook will now run with the SageMath kernel

### Option 2: Create New Notebook with SageMath

1. Create a new Jupyter notebook
2. When prompted to select a kernel, choose **"SageMath"**
3. Start coding with SageMath!

### Option 3: Use SageMath from Command Line

```bash
# Start SageMath interactive shell
sage

# Run a SageMath script
sage script.sage

# Run Python code with SageMath
sage -python script.py

# Get help
sage --help
```

## What Was Installed

- **SageMath 10.7**: Complete mathematical software system
- **SageMath Jupyter Kernel**: Allows running SageMath in Jupyter notebooks
- **All dependencies**: Including gap, pari, maxima, and many mathematical libraries

## Verifying Installation

Run this command to verify:
```bash
sage --version
```

Or check available kernels:
```bash
sage --jupyter kernelspec list
```

## Using SageMath Functions

Your notebook uses functions like:
- `Partitions()`: Integer partition generator
- `Permutations()`: Permutation generator
- And many other SageMath-specific mathematical functions

These will now work correctly when you select the SageMath kernel!

## Troubleshooting

If the kernel doesn't appear:
1. Reload VS Code window (Ctrl+Shift+P → "Developer: Reload Window")
2. Make sure you're selecting the kernel in the notebook (top-right corner)
3. Check that sage is installed: `which sage` should return `/opt/conda/bin/sage`

## Note for Future Codespaces

If you want this setup to persist for new Codespaces, add to `.devcontainer/devcontainer.json`:

```json
{
  "postCreateCommand": "conda install -y -c conda-forge sage jupyter"
}
```

Or create a `.devcontainer/post-create.sh` script with the installation commands.
