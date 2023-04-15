# Chapter 2: Installing Python and Required Packages

Welcome back to our journey towards using Python for Finance. In our previous chapter, we introduced the fundamentals of Python programming language which provided a strong foundation for our financial programming needs. Now that we have a basic understanding of Python, it is time to take the first step towards setting up our development environment.

In this chapter, we will discuss the installation process for Python on various operating systems, including Windows, Mac OS, and Linux. We will also delve into the installation of required packages such as NumPy, Pandas, and Matplotlib that will enable us to perform financial calculations and visualize data. From there, we will cover important aspects such as version control, setting up virtual environments, and configuring an Integrated Development Environment (IDE) for enhanced productivity.

By the end of this chapter, you will have a fully equipped Python development environment that is tailored towards finance, making it easy for you to solve complex financial problems, analyze data and visualize trends. Let's begin!
# Chapter 2: Installing Python and Required Packages

## Introduction
In this chapter, we will guide you through the step-by-step process of setting up a Python development environment with all the necessary packages for financial analysis. We will provide detailed instructions for installing Python and required packages such as NumPy, Pandas, and Matplotlib for Windows, Mac OS, and Linux. 

## Prerequisites
Before we proceed, we assume that you have a basic understanding of the Python programming language. If not, we recommend that you go through the previous chapter on “Introduction to Python for Finance” to get up to speed.

## Installing Python
We will provide detailed instructions on how to install Python on your specific operating systems. Options for installation of Anaconda Python Distribution and Homebrew Package Manager for Mac will be discussed.

## Installing Required Packages
After installing Python, we will show you how to install important packages such as NumPy, Pandas, and Matplotlib via pip, conda and Anaconda Navigator.

## Virtual Environments
Setting up virtual environments allows us to avoid issues with package and version Control. We will explore how to set up virtual environments using venv and Conda, as well as activate and deactivate it.

## Integrated Development Environment
Finally, we will show how to configure an Integrated Development Environment (IDE) for enhanced productivity in finance, such as PyCharm, Jupyter Notebooks or Spyder.

## Conclusion
With the Python Development environment set up, you’ll have everything you need to explore financial data and create powerful analyses. By the end of this chapter, you'll be ready to take the first steps towards financial analysis in Python.
In this chapter, we will focus on the installation of Python and required packages for financial analysis. We will use the following commands to install these packages:

### Installing Python on Windows

1. First, go to https://www.python.org/downloads/windows/ and download the Python installer based on your system architecture (32-bit or 64-bit).
![Download Python on Windows](https://i.imgur.com/fa43CDM.png)

2. Run the installer and select the checkbox “Add Python to PATH” to make Python accessible from any location in the Command Prompt.

3. Choose Customize Installation to customize the components that will be installed. Recommendation is to include pip package.

4. Follow the remaining steps, and once the installation completes, open Command Prompt (cmd) to check whether Python is installed by typing `python`.

### Installing Required Packages

#### Installing packages via pip
1. Open Command Prompt (cmd)
2. Install required package dependencies that are needed for building python packages by running:

    `python -m pip install --upgrade pip wheel setuptools`

3. Install required packages using pip package installer (e.g. pandas, matplotlib and numpy):

    `pip install pandas matplotlib numpy`

#### Installing packages via Conda

1. Open Anaconda Prompt
2. Create a new environment:

    `conda create --name <env-name>`

3. Activate the new environment:

    `conda activate <env-name>`

4. Install required packages in the new environment:

    `conda install pandas matplotlib numpy`
    
#### Installing packages via Anaconda Navigator

1. Open Anaconda Navigator and select the environment you wish to install the package into.

2. Select the "Not Installed" menu and search for the package you wish to install.

3. Select the package and click "Apply" to install the package.

### Virtual Environments

Python’s virtual environment module, venv, allows you to create isolated environments with its own dependencies. Follow the instructions below to create a new virtual environment for your project.

1. Create a new virtual environment:

    `python -m venv <path/to/env>`
    
2. Activate the environment:

    Windows: `<path/to/env>/Scripts/activate.bat`
    
    Mac/Linux: `source <path/to/env>/bin/activate`

3. Once activated, run the following command:

    `pip install pandas matplotlib numpy`
    
4. From here on out, any changes you make will only affect your virtual environment, and you can move or delete the environment folder without affecting your system.

### Integrated Development Environment

An Integrated Development Environment or IDE is a software application that provides comprehensive facilities to computer programmers for writing, testing, and managing code. Popular IDEs in finance include:

- PyCharm
- Jupyter Notebooks 
- Spyder 

There are many IDEs available to choose from with various features that support financial analysis. Install the preferred IDE to enhance and streamline the development process.


[Next Chapter](03_Chapter03.md)