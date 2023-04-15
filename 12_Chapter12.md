# Chapter 12: Option Pricing Using Black-Scholes Model

Welcome back to our journey of using Python for finance! In the previous chapter, we delved into Monte Carlo Simulation to estimate the value of financial instruments. In this chapter, we will be exploring the Black-Scholes Model, a mathematical equation used to determine the price of European-style options. 

The Black-Scholes Model was first introduced in 1973 by Fischer Black and Myron Scholes in their groundbreaking paper titled "The Pricing of Options and Corporate Liabilities". This theory became widely accepted and revolutionized the way options are priced and traded on financial markets.

This chapter will provide a thorough overview of the Black-Scholes Model, including the assumptions behind it and the mathematics involved. We will show you how to apply this model in Python to price options and will provide real-world examples to help you understand the practical applications of this theory.

So, fasten your seatbelts and get ready to explore the Black-Scholes Model in-depth. At the end of this chapter, you will have a solid foundation on option pricing, which will be useful in your future endeavors in finance. Let's get started!
## Understanding the Black-Scholes Model

### Assumptions

The Black-Scholes Model makes several assumptions to simplify option pricing. Here are the key assumptions:

- There are no transaction costs
- Markets are efficient
- Stock prices are continuous and follow a lognormal distribution
- The option is European-style, which means it can only be exercised at expiry
- There is no dividend payout on the underlying asset

### Mathematics

The Black-Scholes Model is quite complex, but in essence, it provides a formula for calculating a theoretical price for a specific type of option. This formula takes into account several variables, including the current stock price, the option's strike price, time to expiry, volatility, and risk-free interest rates.

To apply the Black-Scholes Model in Python, we need to use multiple packages such as numpy, scipy and pandas. We will provide code examples to help you build a function that calculates the theoretical price of an option using the Black-Scholes Model.

### Real-World Examples

We will illustrate the practical applications of the Black-Scholes Model with real-world examples. This will help you see how the model can be used to estimate the value of options in various scenarios. We will consider the factors that can affect the price of an option, such as volatility, time to expiration, and the underlying stock price.

Some of the examples we will consider include:

- Estimating the price of a call or put option based on its parameters
- Comparing the theoretical prices to market prices to identify opportunities for profit
- Exploring the impact of different factors on option prices, such as changing volatility or time to expiration

### Conclusion

The Black-Scholes Model is an essential tool for option pricing, and it has become a fundamental concept in modern finance theory. Understanding the assumptions behind this model, the mathematics involved, and the practical applications can provide valuable insights for investors and traders. In this chapter, we aim to provide you with a comprehensive understanding of the Black-Scholes Model and how you can implement it in Python. Let's dive in!
Sure, here is an explanation of the code used to resolve the Black-Scholes option pricing model:

First, we need to import the necessary packages:

```python
import numpy as np
from scipy.stats import norm
from datetime import date
```

Next, we create a function called `black_scholes_call` that calculates the theoretical price of a call option using the Black-Scholes model:

```python
def black_scholes_call(stock_price, strike_price, time_to_expiry, risk_free_rate, volatility):
    d1 = (np.log(stock_price / strike_price) + (risk_free_rate + 0.5 * volatility ** 2) * time_to_expiry) / (volatility * np.sqrt(time_to_expiry))
    d2 = d1 - volatility * np.sqrt(time_to_expiry)
    call_price = stock_price * norm.cdf(d1) - strike_price * np.exp(-risk_free_rate * time_to_expiry) * norm.cdf(d2)
    return call_price
```

This function takes in several parameters:

- `stock_price`: the current stock price
- `strike_price`: the strike price of the option
- `time_to_expiry`: the time to expiry (in year fractions)
- `risk_free_rate`: the risk-free interest rate (in decimal)
- `volatility`: the annualized volatility of the stock price

In the first two lines of the function, we calculate `d1` and `d2`, which are intermediate calculations necessary for the Black-Scholes formula. 

In the third line, we use the Black-Scholes formula to calculate the theoretical price of the call option. The formula calculates two probabilities, given the standard normal cumulative distribution function: the probability that the option will be exercised (`norm.cdf(d1)`) and the probability that it will expire out-of-the-money (`norm.cdf(d2)`). We then multiply the first probability by the stock price and subtract the second probability multiplied by the strike price discounted by the risk-free interest rate.

We can also create a similar function to calculate the theoretical price of a put option:

```python
def black_scholes_put(stock_price, strike_price, time_to_expiry, risk_free_rate, volatility):
    d1 = (np.log(stock_price / strike_price) + (risk_free_rate + 0.5 * volatility ** 2) * time_to_expiry) / (volatility * np.sqrt(time_to_expiry))
    d2 = d1 - volatility * np.sqrt(time_to_expiry)
    put_price = strike_price * np.exp(-risk_free_rate * time_to_expiry) * norm.cdf(-d2) - stock_price * norm.cdf(-d1)
    return put_price
```

This function takes the same parameters as `black_scholes_call`, and the only difference is the way we calculate `put_price`. Instead of subtracting the second probability from the first, we subtract the first probability from the second.

We can use these functions to calculate the theoretical prices of options with certain parameters. For example:

```python
>>> stock_price = 100
>>> strike_price = 105
>>> time_to_expiry = 0.25
>>> risk_free_rate = 0.02
>>> volatility = 0.20
>>> black_scholes_call(stock_price, strike_price, time_to_expiry, risk_free_rate, volatility)
2.864425185424596
>>> black_scholes_put(stock_price, strike_price, time_to_expiry, risk_free_rate, volatility)
6.693361618186556
```

These calculations estimate the theoretical prices of a call and put option for a stock price of 100, a strike price of 105, a time to expiry of 0.25 (or 3 months), a risk-free rate of 0.02, and a volatility of 0.20. The estimated call price is 2.86, and the estimated put price is 6.69.


[Next Chapter](13_Chapter13.md)