# SCI-TECH-ENGG-NEXUS-Services🔬
# Python Setup Tips🐍
<br>
💡 If You’re Using Google Colab
<br>
If you're running your code on Google Colab (https://colab.research.google.com/), just add this line at the top of your notebook:
<br>
!pip install uv or pip install uv
<br>
You can skip the rest of this guide if you're using Colab.
<br>
🖥️ For Your Local Machine (Laptop/Desktop)
<br>
Here’s how you can manage Python and install packages on your own computer.
<br>
I’ve used Conda (https://colab.research.google.com/) and pip (https://pypi.org/project/pip/), for a long time, but now I recommend a new tool called uv (https://github.com/astral-sh/uv). It's faster and smarter when it comes to installing Python packages and handling dependencies.
<br>
✅ Best Way in 2025: Use uv
<br>
Try Option 1 (uv) first — it's modern and fast. If you run into trouble, you can try Option 2 (Conda) instead.
<br>
🧰 Option 1: Using uv
<br>
Let’s go through the steps to set up Python and install packages using uv.
<br>
Note: uv works like pip, so if you’ve used pip before, this will feel familiar.
<br>
There are also more advanced uv features, like using uv add, but we’ll stick with the basics here.
<br>



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


