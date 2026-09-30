# Numerical Interpolation Methods

This project implements and compares several numerical interpolation methods in Python, including **Lagrange interpolation**, **Newton interpolation**, and **natural cubic spline interpolation**.

The methods are applied to the function

$f(x) = \cos(x) + \sin(x)$

to study interpolation accuracy, numerical error, smoothness, and extrapolation behavior.

## Methods Implemented

- **Lagrange Interpolation**
  - Constructed a degree-4 interpolation polynomial from five data points
  - Implemented the Lagrange basis polynomials from scratch
  - Evaluated interpolation and extrapolation errors
  - Compared actual error with the theoretical interpolation error bound

- **Newton Interpolation**
  - Constructed a cubic Newton polynomial using forward differences
  - Calculated first-, second-, and third-order finite differences
  - Evaluated the polynomial at multiple test points

- **Natural Cubic Spline**
  - Constructed a piecewise cubic spline without using built-in spline functions
  - Formulated the interpolation, derivative continuity, and natural boundary conditions as a linear system
  - Solved the spline coefficients using `numpy.linalg.solve`

## Analysis

The project compares the numerical methods using error tables and visualizations.

Key observations include:

- Interpolation is generally more accurate near or inside the range of the original data points.
- Errors increase when the methods are used for extrapolation.
- The natural cubic spline provides a smooth piecewise approximation with continuous first and second derivatives.
- Newton and spline interpolation show different accuracy depending on the evaluation point.

## Technologies

- Python
- NumPy
- Pandas
- Matplotlib
- Jupyter Notebook

## Example Results

For the Lagrange interpolation polynomial:

| $x$ | True Value | Approximation | Absolute Error |
|---|---:|---:|---:|
| $0.85$ | $1.411264$ | $1.411271$ | $0.000007$ |
| $1.25$ | $1.264307$ | $1.264089$ | $0.000218$ |

The results demonstrate that interpolation at $x = 0.85$ is substantially more accurate than extrapolation at $x = 1.25$.

## Visualization

The project includes plots comparing the original function with the interpolation polynomials and natural cubic spline, illustrating how approximation error changes inside and outside the interpolation interval.
