# Chapter 4: Python Libraries for Finance

Welcome back! In the previous chapter, we discussed the basic programming constructs in Python. Now that we have a good foundation of Python programming, it is time to dive into the world of finance with Python.

Python is becoming increasingly popular in the finance industry because of its flexibility, efficiency, and wide range of libraries. Libraries are pre-written code that allows us to perform complex tasks with just a few lines of code. In this chapter, we will explore some of the most commonly used Python libraries for finance.

We will cover the following Python libraries:

1. NumPy – This library is useful for handling numerical data in finance.
2. pandas – This library is useful for data manipulation and analysis.
3. Matplotlib – This library is useful for creating data visualizations, including charts and graphs.
4. SciPy – This library is useful for scientific computing in finance.

We will also touch on some additional libraries that are commonly used in finance.

By the end of this chapter, you will have a solid understanding of the Python libraries that are essential in finance and be on your way to becoming a proficient finance programmer. Let's get started!
# Chapter 4: Python Libraries for Finance - Exercises

Congratulations on making it this far! In this section, we will put your newfound knowledge to the test with some exercises.

## Exercise 1: NumPy Arrays

1. Create two NumPy arrays: `a = [1, 2, 3, 4, 5]` and `b = [10, 20, 30, 40, 50]`.
2. Add the two arrays element-wise.
3. Multiply the two arrays element-wise.
4. Compute the dot product of the two arrays.

## Exercise 2: pandas DataFrame

1. Create the following pandas DataFrame using the given data:
   
   |  | Name | Age | Gender | Occupation |
   |--|------|-----|--------|------------|
   | 0| John | 25  | Male   | Engineer   |
   | 1| Lisa | 30  | Female | Manager    |
   | 2| Alex | 23  | Male   | Analyst    |

2. Add a new column "Salary" with the following data: [50000, 75000, 40000].
3. Select only the rows where the Age is greater than 25.
4. Group the data based on the Gender and compute the average age of each group.

## Exercise 3: Matplotlib Visualization

1. Create a line plot of the following data using Matplotlib:

   |  | Year | Sales |
   |--|------|-------|
   | 0| 2015 | 100   |
   | 1| 2016 | 120   |
   | 2| 2017 | 150   |
   | 3| 2018 | 200   |
   | 4| 2019 | 180   |

2. Add a label to the x-axis ("Year") and the y-axis ("Sales").
3. Save the plot as a PNG file.

## Exercise 4: SciPy Statistics

1. Create a SciPy normal continuous random variable with mean 5 and standard deviation 2.
2. Generate 1000 random samples from the distribution.
3. Compute the sample mean and sample standard deviation.
4. Compute the 95% confidence interval for the population mean.

Good luck and have fun! Don't hesitate to reference previous sections or use outside resources if necessary.
## Explanation of  Exercises

### Exercise 1: NumPy Arrays

1. We start by creating two NumPy arrays using the `numpy.array()` function.
```python
import numpy as np

a = np.array([1, 2, 3, 4, 5])
b = np.array([10, 20, 30, 40, 50])
```

2. To add the two arrays element-wise, we can simply use the `+` operator on the arrays.
```python
c = a + b
```

3. To multiply the two arrays element-wise, we can use the `*` operator on the arrays. 
```python
d = a * b
```

4. To compute the dot product of the two arrays, we can use the `numpy.dot()` function.
```python
dot_product = np.dot(a, b)
```

### Exercise 2: pandas DataFrame

1. We start by creating a dictionary of the data.
```python
import pandas as pd

data = {'Name': ['John', 'Lisa', 'Alex'],
        'Age': [25, 30, 23],
        'Gender': ['Male', 'Female', 'Male'],
        'Occupation': ['Engineer', 'Manager', 'Analyst']}
```
We then use the `pandas.DataFrame()` function to create the DataFrame.
```python
df = pd.DataFrame(data)
```

2. To add a new column to the DataFrame, we can simply assign a new list of data to a new column name.
```python
df['Salary'] = [50000, 75000, 40000]
```

3. To select only the rows where the Age is greater than 25, we can use boolean indexing.
```python
df[df['Age'] > 25]
```

4. To group the data by Gender and compute the average age of each group, we can use the `pandas.DataFrame.groupby()` and `pandas.DataFrame.mean()` functions.
```python
df.groupby('Gender')['Age'].mean()
```

### Exercise 3: Matplotlib Visualization

1. We start by creating two lists containing the x and y values.
```python
import matplotlib.pyplot as plt

x = [2015, 2016, 2017, 2018, 2019]
y = [100, 120, 150, 200, 180]
```

We then use the `plt.plot()` function to create the line plot.
```python
plt.plot(x, y)
```

2. We can add labels to the x-axis and y-axis using the `plt.xlabel()` and `plt.ylabel()` functions.
```python
plt.xlabel('Year')
plt.ylabel('Sales')
```

3. We can save the plot as a PNG file using the `plt.savefig()` function.
```python
plt.savefig('line_plot.png')
```

### Exercise 4: SciPy Statistics

1. We start by creating a SciPy normal continuous random variable with mean 5 and standard deviation 2 using the `scipy.stats.norm()` function.
```python
from scipy.stats import norm

X = norm(loc=5, scale=2)
```

2. We generate 1000 random samples from the distribution using the `rvs()` method of `X`.
```python
samples = X.rvs(size=1000)
```

3. We compute the sample mean and sample standard deviation using the `numpy.mean()` and `numpy.std()` functions.
```python
sample_mean = np.mean(samples)
sample_std = np.std(samples)
```

4. We compute the 95% confidence interval for the population mean using the `scipy.stats.t.interval()` function.
```python
alpha = 0.05
n = len(samples)
t_value = t.ppf(1 - alpha/2, n-1)
lower = sample_mean - t_value * sample_std / np.sqrt(n)
upper = sample_mean + t_value * sample_std / np.sqrt(n)
```

We use the `alpha` parameter to specify the confidence level (1 - alpha), and the `n-1` parameter in `t.ppf()` to specify the degrees of freedom (n-1). We then calculate the lower and upper bounds of the confidence interval using the formula:

<center>CI = (sample_mean - t_value * sample_std / sqrt(n), sample_mean + t_value * sample_std / sqrt(n))</center> 

where `t_value` is the t-value from the t-distribution with `n-1` degrees of freedom. The `numpy.sqrt()` function is used to calculate the square root of `n`.


[Next Chapter](05_Chapter05.md)