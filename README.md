# Data-Visualization
Use Seaborn or Matplotlib to create: Histogram for at least one numeric column Boxplot to detect outliers Correlation heatmap Pair plot to compare clusters (if applicable)

Data Visualization Project using Seaborn & Matplotlib
This project demonstrates key data visualization techniques using Python libraries Seaborn and Matplotlib. The dataset includes numeric features that are explored through histograms, boxplots, correlation heatmaps, and pair plots.

📁 Project Structure

.
├── data/
│ └── your_dataset.csv
├── visuals/
│ ├── histogram.png
│ ├── boxplot.png
│ ├── correlation_heatmap.png
│ └── pairplot.png
├── data_viz.ipynb
└── README.md

📌 Requirements

Python 3.7+

pandas

seaborn

matplotlib

numpy (if needed)

jupyter (recommended for notebook)

Install requirements via:

pip install pandas seaborn matplotlib

📊 Visualizations Included

Histogram

Visualizes the distribution of a numeric column (e.g., petal_length, age, salary).

Helps understand skewness, frequency, and spread.

Boxplot

Detects outliers and shows median, quartiles, and spread.

Useful for comparing distributions between groups.

Correlation Heatmap

Shows the correlation between all numeric columns.

Helps identify multicollinearity or strongly related features.

Pair Plot (if applicable)

Plots pairwise relationships and distributions across all numeric features.

Useful for cluster analysis and pattern discovery.

🗂 Sample Code Snippet

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

Load dataset
df = pd.read_csv("data/your_dataset.csv")

Histogram
sns.histplot(df['numeric_column'], kde=True)
plt.savefig("visuals/histogram.png")
plt.show()

Boxplot
sns.boxplot(x=df['numeric_column'])
plt.savefig("visuals/boxplot.png")
plt.show()

Correlation heatmap
corr = df.corr()
sns.heatmap(corr, annot=True, cmap="coolwarm")
plt.savefig("visuals/correlation_heatmap.png")
plt.show()

Pair plot
sns.pairplot(df)
plt.savefig("visuals/pairplot.png")
plt.show()
