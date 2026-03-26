# Students-Performance-Analysis
Dataset :
   synthetic dataset 

Objectives :

1,To generate a dataset of students using Python libraries like NumPy, Pandas, and Faker.
2,To analyze student performance by calculating:
Total marks
Average marks
Grades
3,To apply descriptive statistics such as:
Mean
Median
Mode
Standard deviation
4,To classify students into grades (A, B, C, Fail) based on their performance.
5,To identify top-performing students and low-performing (fail) students.
6,To perform group-wise analysis based on:
Department
Gender
Year
7,To analyze relationships between variables like attendance and average marks using correlation.
8,To visualize data using graphs such as:
Bar chart
Histogram
Scatter plot
9, understand patterns and trends in student performance.
10,To improve data analysis skills using Python libraries.

Project Highlights :

Data Preprocessing:

Generated dataset using Python libraries (NumPy, Pandas, Faker)
Cleaned and structured the data
Created new features like Total and Average marks
Converted raw data into a usable format for analysis
Ensured data consistency and quality

Exploratory Data Analysis (EDA):

Used statistical methods: Mean, Median, Mode, Standard Deviation
Identified patterns in student performance
Compared performance across:
Departments
Gender
Year
Found relationships (e.g., Attendance vs Average marks)
Detected trends and variations in the dataset


Machine Learning Model :

Applied basic classification logic (Grade system)
Categorized students into:
A, B, C, Fail
Can be extended to use ML algorithms like:
Logistic Regression
Decision Tree
Helps in predicting student performance

Visualization:

Created visual representations using Matplotlib
Used different charts:
Bar chart → Department-wise performance
Histogram → Distribution of marks
Scatter plot → Attendance vs Average
Made data easy to understand visually
Highlighted key insights and trends


Tools and Technologies :

Python
pandas
numpy
Faker

Results:
     the project was successfully completed using Python. A dataset of students was created and analyzed to understand their performance.
The results show that most students scored average marks, while only a few students got high grades and some failed. The grading system helped to clearly classify students.
The statistical analysis (mean, median, mode) shows that overall student performance is moderate. The comparison between departments, gender, and year shows only small differences.
The analysis also shows that students with good attendance tend to get better marks.
The graphs like bar chart, histogram, and scatter plot helped to easily understand the data and identify patterns.
Overall, the project helps to understand student performance and improves data analysis skills.


plt.scatter(df["Attendance"],df["Average"])
plt.show()
