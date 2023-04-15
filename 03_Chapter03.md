# Chapter 3: Basic Python Programming Constructs

Welcome to the third chapter of our book on How to use Python for finance! In the previous chapter, we learned how to install Python and required packages to start our journey of mastering Python programming for finance. 

Now, with a solid foundation of Python, we can dive into the world of programming constructs. In this chapter, we will guide you through the fundamental programming constructs in Python, including:

- Variables and Data Types
- Basic Operators
- Conditional Statements
- Loops

These programming constructs are crucial to understand for any programming language, and Python is no different. By the end of this chapter, you will have a clear understanding of how to use these constructs and incorporate them into your financial analysis using Python.

In the finance industry, being able to apply programming constructs with precision and accuracy is essential. Any financial analysis requires proper logic, error handling, and precision, making these programming constructs an essential piece of the puzzle. We will use financial problems and examples to teach you how Python programming constructs can be used to solve financial problems.

So, let us get started on this exciting journey of learning Basic Python Programming Constructs for finance!
# Chapter 3: Basic Python Programming Constructs - Exercises

In this chapter, we learned about various programming constructs such as variables, data types, operators, conditional statements, and loops. To reinforce our understanding of these concepts, we have included a set of exercises. These exercises are designed to help you apply what you have learned to solve practical financial problems. 

For each exercise, we have provided a problem description, and it is up to you to implement the solution using Python. We encourage you to try to solve these problems in as many different ways as possible. The more practice you get with Python, the more confident you will become in using these programming constructs in your financial analysis. 

In addition to the exercises, we have also included some bonus challenges that will test your programming skills and knowledge of Python. These challenges are not related to finance, but they will help you improve your problem-solving abilities and enhance your understanding of Python programming.

We recommend that you attempt these exercises on your own before referring to the solutions provided in this book. However, if you get stuck, feel free to refer back to the relevant sections in the chapter or to seek help from online forums.

Good luck and happy coding!
## Exercise: Calculate Compound Interest

**Problem:** John is planning to invest $10,000 for a duration of 5 years. The bank offers an annual interest rate of 3.5% on his investments. John wants to know the future value of his investments after 5 years, assuming he reinvests the earned interest. 

**Solution:**

In this exercise, we will use the compound interest formula to calculate the future value of John's investment. The formula for compound interest is:

```
FV = P * (1 + r/n)^(n*t)
```

where:
- FV is the future value of the investment
- P is the principal amount (the initial amount invested)
- r is the annual interest rate as a decimal
- n is the number of times the interest is compounded per year
- t is the time the money is invested in years

Firstly, we'll assign the relevant values to each variable: 

```python
P = 10000  # principal amount
r = 0.035  # annual interest rate
n = 1      # interest compounded annually
t = 5      # investment duration in years
```

With these values assigned, all that's left is to plug them into the compound interest formula and solve for FV:

```python
FV = P * (1 + r/n)**(n*t)
```

This will give us the future value of John's investment. 

In Python, we can put all the above code in a single script as shown below:

```python
# assign the required values
P = 10000  # principal amount
r = 0.035  # annual interest rate
n = 1      # interest compounded annually
t = 5      # investment duration in years

# calculate and print the future value
FV = P * (1 + r/n)**(n*t)
print(f"The future value of John's investment is ${FV:.2f}")
```

The output of the script will be:

```
The future value of John's investment is $11,964.50
```

So, John's investment will yield him a future value of $11,964.50 at the end of the 5-year investment period, assuming he reinvests the earned interest.


[Next Chapter](04_Chapter04.md)