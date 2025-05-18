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

