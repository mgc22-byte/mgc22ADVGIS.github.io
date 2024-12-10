# Import necessary libraries
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load the dataset
import pandas as pd  # Import pandas library

def load_data(file_path: str) -> pd.DataFrame:
    return pd.read_csv(file_path)

fia_data = load_data(r'U:\Biogeography Classwork\ENTIRE_TREE.csv')  # Load data into a DataFrame
fia_data

# Display the first few rows of the dataset
print(fia_data.head())


# Data Cleaning
# Check for missing values
print(df.isnull().sum())

# Fill missing values or drop rows/columns with missing values
df = df.dropna() # Example: dropping rows with missing values

# Data Exploration
# Summary statistics

print(df.describe())

# Visualize missing values
plt.figure(figsize=(10, 6))
sns.heatmap(df.isnull(), cbar=False, cmap='viridis')
plt.title('Missing Values Heatmap')
plt.show()


# Relationships between variables
plt.figure(figsize=(10, 6))
sns.scatterplot(x='column1', y='column2', data=df)
plt.title('Scatter plot between column1 and column2')
plt.show()


# Visualize the correlation matrix
plt.figure(figsize=(12, 8))
correlation_matrix = df.corr()
sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm', linewidths=0.5)
plt.title('Correlation Matrix')
plt.show()
