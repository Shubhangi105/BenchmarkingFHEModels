# Homomorphic Encryption in Machine Learning

In the digital age, the value of data has become paramount, driving innovation and economic growth across various sectors. However, this surge in data importance raises concerns about privacy and security. While traditional encryption methods secure data during transmission and storage, they often fall short when performing computations without compromising privacy. Homomorphic encryption offers a revolutionary approach to handling sensitive data in data science, allowing computations directly on encrypted data without the need for decryption. Fully Homomorphic Encryption (FHE) stands out as a powerful variant supporting arbitrary computations on encrypted data.

## Overview

This repository explores the comparison of machine learning models on both encrypted and unencrypted data. The evaluation begins with fundamental models such as linear and logistic regression, progressively examining these models from an encryption perspective. The study extends to XGBoost applied to sentiment analysis on encrypted data encoded by TF-IDF vectorization and a Transformer. Additionally, we delve into non-linear models, constructing an encrypted neural network and an attention-encrypted transformer.

## Results

Execution times for different model versions with varying levels of homomorphic encryption:

```
| Model                        | Version        | Execution time (s)       |
|------------------------------|----------------|--------------------------|
| Linear Regression            | FHE-disable    | 1.8224 X 10^{-4}         |
|                              | FHE-simulate   | 9.4503 X 10^{-4}         |
|                              | FHE-execute    | 6.1006 X 10^{-4}         |
| Logistic Regression          | FHE-disable    | 2.7689 X 10^{-4}         |
|                              | FHE-simulate   | 9.1355 X 10^{-4}         |
|                              | FHE-execute    | 4.2944 X 10^{-3}         |
| XGBoost on TF-IDF vectorized | FHE-disable    | 0.0225                   |
|                              | FHE-simulate   | 0.0242                   |
|                              | FHE-execute    | 45.7622                  |
| XGBoost on transformer       | FHE-disable    | 0.0167                   |
| vectorized                   | FHE-simulate   | 0.0628                   |
|                              | FHE-execute    | 9.3957                   |
| Neural Network               | FHE-disable    | 0.2300                   |
|                              | FHE-simulate   | 0.0181                   |
|                              | FHE-execute    | 182.9603                 |
| Encryption attention head    | FHE-disable    | 0.1515                   |
|                              | FHE-simulate   | 0.1321                   |
|                              | FHE-execute    | 25.0309                  |
```

## Acknowledgment

This work was inspired by Zama AI's Concrete ML library. Their contributions served as a foundation and inspiration for much of our work. We extend our gratitude to Zama AI for their valuable insights and resources.

## Purpose

The primary objective is to assess the viability of current homomorphic encryption solutions for data scientists. By providing insights into the practicality of employing these techniques, this study aims to contribute to the understanding of the intersection between homomorphic encryption and machine learning.
