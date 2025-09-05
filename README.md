# Monte-Carlo Simulations for European Call Options Pricing
This repository contains the Python code for a Monte Carlo simulation model designed to price European call options. The model simulates thousands of potential stock price paths to estimate the value of an options contract, providing a robust framework for financial analysis. This project was developed as part of a research paper on the application of Monte Carlo methods in options trading.

--- 🎯 Project Goals
-Implement a Monte Carlo simulation model to price European call options.
-Explore the mathematical foundations of the model, including solving a Stochastic Differential Equation (SDE) using Ito's Lemma and discretising it for numerical simulation.
-Simulate thousands of stock price paths to calculate the expected payoff of a European call option.
-Evaluate the model's strengths and limitations, considering factors like parameter sensitivity, computational cost, and real-world market constraints.

--- 🔍 Overview
1. Mathematical Foundation: The model is built on the geometric Brownian motion SDE, which is solved to derive a formula for predicting stock prices over time. This continuous model is then discretized to allow for step-by-step simulation.

2. Simulation: The Python code simulates a large number of independent stock price paths, with each step in the path incorporating a random variable drawn from a normal distribution.

3. Pricing: The final stock prices from all simulations are used to calculate the payoff of the European call option. The average of these payoffs is then discounted to present value to estimate the option's price.

4. Visualisation: The results are visualised through graphs showing the simulated asset price paths and a histogram of the final asset prices at maturity.

--- 🛠️ Tech Stack
-**Python** (NumPy, Matplotlib)

---💻 Usage
To run the simulation, you can execute the Python script.

Key Parameters
You can adjust the following parameters within the monte_carlo_options.py file to customize your simulations:

-S_0: Initial stock price
-K: Strike price
-T: Time to maturity (in years)
-r: Risk-free rate
-sigma: Volatility of the asset
-N: Number of simulations (paths)
-M: Number of time steps (daily steps)

The script will output the simulated European call option price and display a plot of the simulated price paths and a histogram of the final prices.
