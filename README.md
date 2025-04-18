Exp 2 : Perform Exploratory Data Analysis (EDA) with Email Dataset
AIM:
To perform Exploratory Data Analysis (EDA) on an email dataset by importing it into a Pandas DataFrame, visualizing it, and extracting meaningful insights.
EQUIPMENTS REQUIRED:
Python 3.x
Jupyter Notebook / Google Colab / VS Code
Libraries: pandas, matplotlib, seaborn
ALGORITHM:
Import the required libraries.
Load the dataset from a URL.
Explore the dataset shape, column names, and types.
Handle missing data.
Perform basic statistical analysis.
Visualize top email senders.
Time-based analysis if a timestamp is present.

Program:

# Step 1: Import required libraries
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Step 2: Load email dataset from URL
url = "https://raw.githubusercontent.com/fivethirtyeight/data/master/email-women/email.csv"
df = pd.read_csv(url)

# Step 3: Basic info
print("Dataset Shape:", df.shape)
print("\nFirst 5 Rows:\n", df.head())
print("\nColumn Names:", df.columns)
print("\nData Types:\n", df.dtypes)

# Step 4: Check for missing values
print("\nMissing Values:\n", df.isnull().sum())

# Step 5: Top 10 email senders
top_senders = df['sender'].value_counts().head(10)
print("\nTop 10 Email Senders:\n", top_senders)

# Step 6: Visualize top email senders
plt.figure(figsize=(10, 6))
sns.barplot(x=top_senders.values, y=top_senders.index, palette='viridis')
plt.title("Top 10 Email Senders")
plt.xlabel("Number of Emails")
plt.ylabel("Sender")
plt.tight_layout()
plt.show()

# Step 7: If 'timestamp' column exists, perform time-based analysis
if 'timestamp' in df.columns:
    df['timestamp'] = pd.to_datetime(df['timestamp'], errors='coerce')
    df['date'] = df['timestamp'].dt.date
    daily_emails = df['date'].value_counts().sort_index()
    
    plt.figure(figsize=(12, 6))
    daily_emails.plot()
    plt.title("Email Activity Over Time")
    plt.xlabel("Date")
    plt.ylabel("Number of Emails")
    plt.xticks(rotation=45)
    plt.tight_layout()
    plt.show()


EXPECTED OUTPUT:
Dataset shape and column summary
Top 10 email senders printed
Bar chart showing top senders
Line chart showing email activity over time (if timestamps are present)

RESULT:
EDA on the email dataset was successfully performed. Insights such as the top senders and email frequency over time were visualized using charts.
