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

# Import Dependencies
Import dependencies for the project
```
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt
```

# Exploratory Data Analysis
1. Load the dataset:
```
df = sns.load_dataset('titanic')
```

2. Inspect the data:
```
print(df.head(10))
print(df.shape)
print(df.dtypes)
```

3. Initial Descriptive Statistics
```
print(df.describe())
```

4. Initial Data Distribution for Numerical Columns
```
df['sepal_length'].hist()
df.hist()
plt.show()
```

5. Initial Data Distribution for Categorical Columns
```
# Inspect value counts by categorical column
df['species'].value_counts()

# Inspect value counts for all categorical columns
for col in df.select_dtypes(include=['object', 'category']).columns:
    # Display count plot
    sns.countplot(x=col, data=df)
    plt.title(f'Distribution of {col}')
    plt.show()

# Show all plots
plt.show()
```

6. Initial Data Transformation and Feature Engineering
Rename a column:
```
df.rename(columns={'fare': 'ticket_price'}, inplace=True)
```
Add a new column:
```
inflation_rate = 14214.51 / 100  # 14,214.51% inflation rate in England since 1912 according to ChatGPT
df['inflated_price'] = round(df['ticket_price'] * (1 + inflation_rate), 2) # add new column 'inflated_price' which calculates the inflated ticket prices
```

7. Initial Visualizations
Each subsection should have the following parts:
Goal: The question you are exploring.
Chart Type: Tell us what kind of chart you choose to illustrate this goal.
Chart: Display the chart.
Story: Use Markdown cell(s) to document your observations and insights.
   

