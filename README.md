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

# Option 1: Using uv🧰 
<br>
Let’s go through the steps to set up Python and install packages using uv.
<br>
Note: uv works like pip, so if you’ve used pip before, this will feel familiar.
<br>
There are also more advanced uv features, like using uv add, but we’ll stick with the basics here.
<br>
1️⃣ Install Python (If You Don't Have It Yet)
<br>
If you've never installed Python manually, it’s a good idea to do it now. This avoids possible issues with your system’s built-in Python.
<br>
Even if you already have Python, check the version by running this command in your terminal:
<br>
python --version
<br>
If it shows Python 3.10 or newer, you’re good to go.
<br>
If not, try this command too:
<br>
python3 --version
<br>
👉 Tip: For best results, use a Python version that’s about 2 versions behind the latest.
For example, if the latest is Python 3.15, go with 3.13 or 3.12. This makes things like PyTorch work better.
<br>
Windows Users:
<br>
Download and run the Python installer from the official website:
🔗 https://www.python.org/downloads/
<br>
🐍 2️⃣ Create a Virtual Environment (Highly Recommended)
Installing packages in a virtual environment keeps your system clean and avoids interfering with system-wide packages.
<br>
Step-by-step:
<br>
1. Install uv:
<br>
pip install uv
<br>
2. Create the virtual environment:
<br>
uv venv --python=python3.13
<br>
This will create a .venv folder in your current directory.
<br>
3. Activate the virtual environment:
<br>
On macOS/Linux:
<br>
source .venv/bin/activate
<br>
On Windows:
<br>
.venv\Scripts\activate
<br>
or
<br>
source .venv/Scripts/activate
<br>
🔁 Important Reminder:
<br>
You need to activate your virtual environment every time you open a new terminal or restart your computer.
<br>
Just run:
<br>
source .venv/bin/activate
<br>
(or the correct command for your OS) inside your project folder to get back to work.
<br>
# Option 2: Using Conda (Anaconda or Miniconda)🧪
<br>
If you prefer not to use uv or run into any issues, Conda is a reliable and widely-used alternative for managing Python environments and packages.
<br>
🐍 What is Conda?
Conda is a package and environment manager that makes it easy to:
<br>
Create isolated environments for different projects
<br>
Install Python and packages in one step
<br>
Avoid version conflicts
<br>
You can install Conda by downloading either:
<br>
Anaconda (comes with many scientific packages)
<br>
🔗 https://www.anaconda.com/products/distribution
<br>
Miniconda (lightweight version, recommended if you want to install only what you need)
<br>
🔗 https://docs.conda.io/en/latest/miniconda.html
<br>
🔧 Steps to Set Up Python Using Conda
<br>
✅ Step 1: Install Miniconda or Anaconda
<br>
Download and run the installer for your operating system.
<br>
During setup, check the box that says "Add Conda to PATH" if available.
<br>
🧪 Step 2: Create a Conda Environment
<br>
In your terminal (VS Code or system terminal), run:
<br>
conda create -n myenv python=3.10
<br>
Replace myenv with whatever name you want for your environment.
<br>
🚀 Step 3: Activate the Environment
<br>
Once created, activate it like this:
<br>
conda activate myenv
<br>
You’ll now see the environment name in your terminal, showing you’re inside the environment.
<br>
📦 Step 4: Install Your Packages
<br>
Now you can install packages using either:
<br>
conda install numpy pandas matplotlib
<br>
Or if you prefer pip, it also works inside Conda environments:
<br>
pip install torch transformers
<br>
🔁 Reminder:
<br>
Every time you open a new terminal or VS Code session, don’t forget to activate your environment again:
<br>
conda activate myenv
<br>
# uv vs conda: A Quick Comparison
<br>
Feature / Task	uv (Modern)	conda (Traditional)
<br>
🐍 Python Installation	External (use python.org or system)	Built-in: installs Python with env
<br>
📦 Package Manager	Uses pip under the hood	Uses conda or pip
<br>
🧪 Environment Creation	uv venv --python=python3.10	conda create -n env python=3.10
<br>
🚀 Environment Activation	source .venv/bin/activate (Unix)	conda activate env
<br>
⚡ Speed	Faster installs, smarter resolver	Slower, but stable
<br>
🌍 Cross-platform Support	Yes (uses virtualenv under the hood)	Yes (very mature)
<br>
🧠 Learning Curve	Low for pip users	Very beginner-friendly
<br>
🔄 Reproducibility (lock files, etc.)	Built-in via uv (advanced users)	Needs conda-lock or manual tracking
<br>
🔌 Integration with Other Tools	Compatible with pip, venv, etc.	Great for data science tools like Jupyter
<br>
🔧 Python Version Flexibility	Python must be installed separately	Python version bundled with env creation
<br>
✅ Which One Should You Use?
<br>
Your Situation	Recommended Tool
<br>
🆕 Beginner or prefer easy setup	Conda
<br>
⚡ Want faster installs, modern tools	uv
<br>
🧪 Need precise Python versioning, system compatibility	Conda
<br>
📦 Already familiar with pip/venv	uv






| Feature / Task                        | `uv` (Modern)                        | `conda` (Traditional)                     |
| ------------------------------------- | ------------------------------------ | ----------------------------------------- |
| 🐍 Python Installation                | External (use python.org or system)  | Built-in: installs Python with env        |
| 📦 Package Manager                    | Uses `pip` under the hood            | Uses `conda` or `pip`                     |
| 🧪 Environment Creation               | `uv venv --python=python3.10`        | `conda create -n env python=3.10`         |
| 🚀 Environment Activation             | `source .venv/bin/activate` (Unix)   | `conda activate env`                      |
| ⚡ Speed                               | Faster installs, smarter resolver    | Slower, but stable                        |
| 🌍 Cross-platform Support             | Yes (uses virtualenv under the hood) | Yes (very mature)                         |
| 🧠 Learning Curve                     | Low for `pip` users                  | Very beginner-friendly                    |
| 🔄 Reproducibility (lock files, etc.) | Built-in via `uv` (advanced users)   | Needs `conda-lock` or manual tracking     |
| 🔌 Integration with Other Tools       | Compatible with `pip`, `venv`, etc.  | Great for data science tools like Jupyter |
| 🔧 Python Version Flexibility         | Python must be installed separately  | Python version bundled with env creation  |


