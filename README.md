# Shor's Algorithm

## Project Overview

This project implements a quantum algorithm for finding the period of a modular exponentiation function. The core idea is based on the principles of quantum computing, specifically utilizing quantum phase estimation to determine the period of the function \( g^x \mod N \), where \( g \) is a chosen integer and \( N \) is the product of two prime numbers.

### Key Concepts

- **Period Finding**: The project focuses on finding the smallest integer \( r \) such that \( g^r \mod N = 1 \). This is achieved by identifying the cycle in the remainders when repeatedly exponentiating \( g \) modulo \( N \).
- **Quantum Phase Estimation**: The quantum circuit is constructed to perform controlled multiplication and utilizes the inverse Quantum Fourier Transform (QFT) to extract the period information from the quantum state.

### Implementation

1. **Classical Period Finding**: The initial part of the project uses classical methods to compute and visualize the remainders of \( g^x \mod N \) for a specified range of \( x \).
2. **Quantum Circuit Construction**: A quantum circuit is built to implement controlled multiplications and the inverse QFT to measure the phases corresponding to the period.
3. **Simulation**: The quantum circuit is executed using the Qiskit Aer simulator, and the results are visualized through a histogram of the measured phases.

### Example

The implementation is tested with:
- \( N = 15 \)
- \( g = 7 \)

## Limitations

- The current implementation only works for \( N = 15 \). Adjustments would be needed to extend this algorithm to other values of \( N \).
