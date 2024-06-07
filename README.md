# datafun-06-eda

# Overview
Project 6 is an opportunity to create your own custom exploratory data analysis (EDA) project using GitHub, Git, Jupyter, pandas, Seaborn and other popular data analytics tools.

# Start a New Project in GitHub & Clone it
In your browser, create a GitHub project repository with a default README.md. Clone your new repository down to your machine where you want your root project folder to be by running the following:
```
git clone URL
```

# Add .gitignore file
Use VS Code to create a new file with the name .gitignore and add at least the following entries:
```
.venv/
.vscode/
```

# Add empty requirements.txt file
Create an empty txt file in your root project folder

# Edit README.md
Edit your README.md file to record your commands, process, and notes. Use one hash space for the title.

# Git Add / Commit / Push to GitHub
Use your terminal to add your files to source control, commit your changes to git, and push them up to GitHub by running the following:
```
git add .
git commit -m "initial commit"
git push origin main
```

# Create and Activate Project Virtual Environment
Use your terminal to create your project virtual environment by running venv as a Python module (python -m venv) and providing the name the destination folder for the project virtual environment as .venv by running the following:
```
py -m venv .venv
.venv\Scripts\Activate
```

# Install Packages into Active Environment
Windows command to install project dependencies:
```
py -m pip install jupyterlab pandas pyarrow matplotlib seaborn
```

# Update requirements.txt
Run the following:
```
python -m pip freeze > requirements.txt
```

# Git add / commit / push
