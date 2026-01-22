# Dataset: IoT Networks - Jamming & Spoofing Detection

## Overview
This repository holds a dataset (generated synthetically) for the ongoing research paper called:

**"Jamming & Spoofing Detection in IoT Networks"**

The dataset is designed to assist in the machine learning detection of wireless attacks against the IoT environment. It was developed to represent regular communication patterns, including both forms of wireless attack: **jamming attacks** and **spoofing attacks**.

The availability of the dataset publicly increases transparency, reproducibility, and future studies.  
 *The attached research article has not been published yet, it is currently being submitted to a conference.*

---

## File Structure
- `simulated_netdata.csv` - the dataset
- `README.md` - documentation for the dataset

---

## How Was This Dataset Generated?
The dataset was generated **synthetically** through the use of the Python controlled simulation approach.  
Statistical distributions for the generation of the dataset were selected to appropriately simulate various aspects of how the network functions under differing levels of a range of conditions.

### Generation Method
- Each class contains **5000 samples**.
- Total number of samples: **15000**.
- Random seed set (`np.random.seed(42)`) for reproducibility.
- Separate statistical models were used for each class:
  - **Normal Traffic**: stable communication, high SNR, low packet loss.
  - **Spoofing Attacks**: abnormal packet behavior, moderate packet loss, identity discrepancies.
  - **Jamming Attacks**: extreme interference, low SNR, high packet loss.

The dataset was created from probabilistic models using the following probability distributions:
- Exponential
- Poisson
- Normal
