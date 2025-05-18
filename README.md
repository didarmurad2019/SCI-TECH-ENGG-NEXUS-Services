# SCI-TECH-ENGG-NEXUS-Services
# Python Setup Tips
<br>
There are several ways to install Python and set up your computing environment. Here, I share my personal preferences.
<br>
Note: If you are running any of the notebooks on Google Colab (https://colab.research.google.com/) and want to install the dependencies, simply run the following code in a new cell at the top of the notebook and skip the rest of this tutorial: pip install uv
<br>
The remaining sections below describe how you can manage your Python environment and packages on your local machine.
<br>
I have been a long-time user of Conda (https://anaconda.org/anaconda/conda) and pip (https://pypi.org/project/pip/), but recently, the uv package (https://github.com/astral-sh/uv) has gained significant traction as it provides a faster and more efficient way to install packages and resolve dependencies.
<br>
I recommend starting with Option 1: Using uv as it is the more modern approach in 2025. If you encounter problems with Option 1, consider Option 2: Using Conda.
<br>
I recommend starting with Option 1: Using uv as it is the more modern approach in 2025. If you encounter problems with Option 1, consider Option 2: Using Conda.
<br>

# Option 1: Using uv
<br>
This section guides you through the Python setup and package installation procedure using uv via its uv pip interface. The uv pip interface may feel more familiar to most Python users who have used pip before than the native uv commands.
<br>
Note: There are alternative ways to install Python and use uv. For example, you can install Python directly via uv and use uv add instead of uv pip install for even faster package management.

# 1. Install Python (if not installed)
<br>
If you haven't manually installed Python on your system before, I highly recommend doing so. This helps prevent potential conflicts with your operating system's built-in Python installation, which could lead to issues.
<br>
However, even if you have installed Python on your system before, check if you have a modern version of Python installed (I recommend 3.13 or newer) by executing the following code in the terminal:
python --version
<br>
If it returns 3.10 or newer, no further action is required.
<br>
Note: If python --version indicates that no Python version is installed, you may also want to check python3 --version since your system might be configured to use the python3 command instead.
<br>
Note: I recommend installing a Python version that is at least 2 versions older than the most recent release to ensure PyTorch compatibility. For example, if the most recent version is Python 3.15, I recommend installing version 3.13 or 3.12.
<br>
Otherwise, if Python is not installed or is an older version, you can install it for your operating system as described below.
<br>

🐍 
# Create a Virtual Environment (Recommended)


