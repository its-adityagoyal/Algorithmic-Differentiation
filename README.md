# Efficient Greek calculation using AAD

## What is Algorithmic Differentiation?
Algorithmic Differentiation (AD), also known as Automatic Differentiation, is a set of techniques to evaluate the derivative of a function specified by a computer program. Unlike symbolic differentiation or numerical approximation, AD applies the chain rule systematically at the elementary operation level, allowing exact derivatives to be computed efficiently and accurately.

## Why Algorithmic Differentiation?
- Provides exact derivatives up to machine precision.
- More efficient and accurate than finite difference method.

## Features of this Repository
- Implementation of Forward and Reverse mode AD.
- Examples demonstrating differentiation of complex functions.
- Calculates Option Greeks efficiently using adjoint (reverse) mode differentiation with the Black-Scholes formula.

## Forward (Tangent) Mode
Tangent mode computes price sensitivities to one input at a time and we must call the tangent method several times, once for each input parameter. This means we can only get one derivative output at a time. So, to compute the derivative of each input parameter we need to call it several times, once for each input parameter.

## Reverse (Adjoint) Mode (AAD)
When using adjoint mode we differentiate code in reverse order, starting with function outputs. Adjoint mode follows the reverse order of the original program. This method shifts one function output at a time and generates derivatives exactly to machine precision for all price inputs in one go. 

## Getting Started

To use the code, clone the repository and install the dependencies listed in `requirements.txt`.

```bash
git clone https://github.com/its-adityagoyal/Efficient-Greeks-AAD.git
cd Efficient-Greeks-AAD
pip install -r requirements.txt


