# Trust Region Framework Based Optimization of Double T-Shaped Antenna

## Overview

This project implements a **Trust Region Framework (TRF)** to optimize the design parameters of a **Double T-shaped Monopole Antenna**. The goal is to enhance antenna performance in terms of return loss, bandwidth, gain, and radiation efficiency for target frequency bands (e.g., Wi-Fi, 5G). The antenna should operate in two frequency bands 2.4-3 GHz and 3.15-6 GHz.

## Motivation

Conventional optimization techniques often struggle with the highly non-linear, multi-modal nature of antenna design problems. The Trust Region Framework offers a robust, iterative method for local optimization, enabling better convergence and model reliability, especially when dealing with parameter-sensitive antenna geometries like the double T-shaped structure. 

## Procedure
- Parametric analysis is performed and data including frequency and (`S11`) parameter is extracted.
- FOM is calculated at all frequencies and stored in csv named ```ml_dataset_with_fom.csv```
- ANN, KNN and LASSO is applied on it to obtain  intermediate dimensions.
- Results from each ML technique is averaged and fed to TRFO.
  
## Optimization Objective

The objective function typically includes:

- Minimization of return loss (`S11`) at the desired operating frequency
- Maximization of bandwidth
- Constraints on size and manufacturability

