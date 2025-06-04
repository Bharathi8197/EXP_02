**Exp 2 : Perform Exploratory Data Analysis (EDA) with Email Dataset**

**AIM:**
To perform Exploratory Data Analysis (EDA) on an email dataset by importing it into a Pandas DataFrame, visualizing it, and extracting meaningful insights.

**EQUIPMENTS REQUIRED:**
Python 3.x
Jupyter Notebook / Google Colab / VS Code
Libraries: pandas, matplotlib, seaborn

**ALGORITHM:**
1)Import the required libraries.
2)Load the dataset from a URL.
3)Explore the dataset shape, column names, and types.
4)Handle missing data.
5)Perform basic statistical analysis.
6)Visualize top email senders.
7)Time-based analysis if a timestamp is present.


**Program:**

# Step 1: Import required libraries
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Step 2: Load email dataset from URL
url = "https://raw.githubusercontent.com/fivethirtyeight/data/master/email-women/email.csv"
df = pd.read_csv(url)

# Step 3: Basic info


# Step 4: Check for missing values


# Step 5: Top 10 email senders


# Step 6: Visualize top email senders


# Step 7: If 'timestamp' column exists, perform time-based analysis

    

**EXPECTED OUTPUT:**
**Note** : Upload the following output screenshots
    Dataset shape and column summary
    Top 10 email senders printed
    Bar chart showing top senders
    Line chart showing email activity over time (if timestamps are present)

**RESULT:**
EDA on the email dataset was successfully performed. Insights such as the top senders and email frequency over time were visualized using charts.
