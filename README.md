# ABC Company Employee Data Analysis

A comprehensive data analysis project analyzing employee demographics, team distribution, positions, age groups, and salary patterns for ABC Company.

## 📊 Project Overview

This project analyzes a dataset of 458 employees across 9 columns to provide detailed insights into the company's workforce structure, salary distribution, and demographic patterns. The analysis includes data preprocessing, exploratory data analysis (EDA), and visualization of key metrics.

## 🎯 Project Objectives

The analysis aims to answer the following business questions:

1. **Team Distribution Analysis**
   - Count of employees in each team
   - Percentage distribution of employees across teams

2. **Position Segregation**
   - Distribution of employees across different positions
   - Position-wise employee count

3. **Age Group Analysis**
   - Identify the predominant age group in the organization
   - Age distribution patterns

4. **Salary Expenditure Analysis**
   - Identify teams with highest salary spending
   - Position-wise salary analysis
   - High-cost team-position combinations

5. **Age-Salary Correlation**
   - Statistical correlation between age and salary
   - Visual representation of the relationship

## 📁 Dataset Information

- **Total Records**: 458 rows
- **Total Features**: 9 columns
- **Company**: ABC Company

### Dataset Columns
- Employee ID
- Team
- Position
- Age
- Height (corrected during preprocessing)
- Salary
- Other demographic information

## 🔧 Data Preprocessing Steps

### 1. Data Cleaning
- Handling missing values
- Checking for duplicate records
- Data type conversions

### 2. Height Column Correction
The `height` column contained incorrect data. Preprocessing steps included:
```python
# Replace height column with random values between 150 and 180
import numpy as np
df['height'] = np.random.randint(150, 181, size=len(df))
```

### 3. Data Validation
- Outlier detection
- Data consistency checks
- Feature engineering (if applicable)

## 📈 Analysis Performed

### 1. Team Distribution Analysis
- Calculated employee count per team
- Computed percentage distribution
- Created visualizations (bar charts, pie charts)

### 2. Position-Based Segregation
- Grouped employees by position
- Analyzed position distribution
- Identified most common positions

### 3. Age Group Analysis
- Created age bins/categories
- Identified predominant age groups
- Visualized age distribution (histograms, box plots)

### 4. Salary Expenditure Analysis
- Team-wise salary aggregation
- Position-wise salary analysis
- Combined team-position salary spending
- Identified high-cost combinations

### 5. Age-Salary Correlation
- Calculated Pearson correlation coefficient
- Created scatter plots with trend lines
- Generated heatmaps for correlation matrix

## 🛠️ Technologies Used

- **Python 3.x**
- **Libraries**:
  - `pandas` - Data manipulation and analysis
  - `numpy` - Numerical computations
  - `matplotlib` - Data visualization
  - `seaborn` - Statistical visualizations
  - `scipy` - Statistical analysis (optional)

## 📊 Key Visualizations

1. **Team Distribution**
   - Bar chart showing employee count per team
   - Pie chart showing percentage distribution

2. **Position Analysis**
   - Horizontal bar chart of positions
   - Count plot for position distribution

3. **Age Group Distribution**
   - Histogram with age bins
   - Box plot for age statistics

4. **Salary Analysis**
   - Grouped bar charts for team-wise salary
   - Heatmap for team-position salary spending

5. **Correlation Analysis**
   - Scatter plot: Age vs Salary
   - Regression line showing trend
   - Correlation matrix heatmap

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn
```

### Installation & Usage

1. Clone the repository:
```bash
git clone <repository-url>
cd employee-data-analysis
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Run the analysis:
```bash
python employee_analysis.py
```

Or open the Jupyter Notebook:
```bash
jupyter notebook Employee_Analysis.ipynb
```

## 📋 Key Findings

> **Note**: Add your specific findings here after completing the analysis

### Example Findings:
- Most employees belong to the [X-Y] age group
- [Team Name] has the highest number of employees ([X]%)
- [Position Name] is the most common position
- Highest salary spending is in [Team] - [Position] combination
- Correlation coefficient between age and salary: [value]

## 📊 Sample Code Snippets

### Team Distribution Analysis
```python
# Calculate team distribution
team_counts = df['Team'].value_counts()
team_percentage = (team_counts / len(df)) * 100

# Visualize
plt.figure(figsize=(10, 6))
team_percentage.plot(kind='bar')
plt.title('Team Distribution (%)')
plt.xlabel('Team')
plt.ylabel('Percentage')
plt.show()
```

### Age-Salary Correlation
```python
# Calculate correlation
correlation = df['Age'].corr(df['Salary'])

# Scatter plot
plt.figure(figsize=(10, 6))
plt.scatter(df['Age'], df['Salary'], alpha=0.5)
plt.title(f'Age vs Salary (Correlation: {correlation:.2f})')
plt.xlabel('Age')
plt.ylabel('Salary')
plt.show()
```

## 🎓 Learning Outcomes

- Data preprocessing and cleaning techniques
- Exploratory Data Analysis (EDA)
- Statistical analysis and correlation
- Data visualization using matplotlib and seaborn
- Deriving business insights from data
- Creating comprehensive data reports

## 👨‍💻 Author

**Devikrishna545**
- GitHub: [@Devikrishna545](https://github.com/Devikrishna545)

## 📝 Course Information

This project was completed as part of:
- **Course**: Data Science and Machine Learning
- **Platform**: Entri
- **Project Type**: Data Analysis Project

## 📄 License

This project is created for educational purposes as part of the Entri Data Science and Machine Learning course.

## 🤝 Acknowledgments

- Entri Team for the comprehensive course curriculum
- ABC Company dataset for analysis
- Python and open-source community for amazing libraries

---

**Note**: This is an educational project created for learning purposes. The dataset and analysis are part of a course assignment.
