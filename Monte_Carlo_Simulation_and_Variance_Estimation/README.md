
# Monte Carlo Simulation and Variance Estimation

This project demonstrates the use of Monte Carlo simulation to estimate the expected value of a given expression. The project also includes variance estimation and visualization.

Variance estimation is crucial because, in real-world applications, we are often constrained by time and computational power. Efficiently conducting Monte Carlo simulations is essential. By estimating the variance of our estimator, we can employ advanced techniques such as antithetic variables and importance sampling to enhance the efficiency of our Monte Carlo simulations. (There will be another document sharing details about these techniques.)

In this project, we use `max(N^3 - K, 0)` as the example, where N is a normally distributed random variable.

For the following graph, the plane is colored according to the expectation values, with the corresponding colors shown in the color bar on the right-hand side.

![Expectation of max(N^3 - K, 0) for different K and Sigma](graph/expectation_different_K_and_sigma.png)

## Project Structure

### Monte Carlo Estimation
The goal is to determine the expected value of `max(N^3 - K, 0)` , where:
- `N` is a normal random variable with a mean of one and standard deviation of three.
- `K` is a given positive constant.

The expression for the expectation is:

`\theta = E[(N^3 - K)^+]`

![Expectation of max(N^3 - K, 0) for different K and Sigma](graph/variance_different_sample_sizes.png)
![Expectation of max(N^3 - K, 0) for different K and Sigma](graph/sample_size_given_precision_level.png)


### Implementation
The project includes a function `MC_theta` to perform the static Monte Carlo approximation for the expectation of \(\max(N^3 - K, 0)\).

#### Function: `MC_theta`
**Inputs:**
- `mu`: Mean of the normal random variable \(N\).
- `sigma`: Standard deviation of \(N\).
- `K`: Parameter in the function.
- `n`: Monte Carlo sample size.
- `seed`: Random seed parameter for reproducibility.

**Outputs:**
- Estimation of the expectation of \(\max(N^3 - K, 0)\).

### Visualization
The project includes visualizations to illustrate the distribution of the simulated values and the resulting estimations.
