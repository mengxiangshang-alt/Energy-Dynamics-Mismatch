# Energy-Dynamics-Mismatch
Yawning reveals energy-dynamics mismatch and neural inertia across state transitions
# \[!\[Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/release/python-380/)

# \[!\[License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

# \[!\[Data Availability](https://img.shields.io/badge/Data-Available-success)](#data-availability)

# 

# This repository contains the official data sharing plans, computational pipelines, and documentation required to reproduce the findings in the manuscript: \*"Yawning reveals energy-dynamics mismatch and neural inertia across state transitions"\*. 

# 

# Our research investigates the micro-scale neural dynamics of yawning across different arousal states (e.g., propofol anesthesia and wakefulness). Utilizing Beagle dog models and cross-species validation in humans, we combined multi-channel EEG recordings with advanced signal processing to uncover the Energy-Dynamics Mismatch (EDM) and neural inertia phenomena.

# 

# \---

# 

# \## 📂 Repository Structure

# 

# The repository is organized into three main directories to ensure full reproducibility and logical flow:

# 

# \### 1. `/Code`

# Contains the 15 core Python scripts used for the analytical pipeline, covering everything from raw EEG preprocessing to complex machine learning predictions and Linear Mixed-Effects (LME) statistical modeling.

# 

# \* \*\*Preprocessing \& State Space Mapping\*\*

# &#x20; \* `01\_eeg\_preprocessing.py`: Automated EEG filtering, artifact rejection, and ICA.

# &#x20; \* `02\_neural\_state\_distance\_gam.py`: GAM smoothing of neural state distances relative to Loss of Consciousness (LOC).

# \* \*\*Clustering \& Micro-scale Dynamics\*\*

# &#x20; \* `03\_kmeans\_umap\_clustering.py`: Unsupervised K-Means clustering and UMAP visualization of yawning-related dynamics.

# &#x20; \* `04\_lzc\_complexity.py`: Sliding window Lempel-Ziv Complexity (LZC) and adaptive permutation testing.

# &#x20; \* `05\_emd\_hht\_analysis.py`: Empirical Mode Decomposition (EMD) and Hilbert-Huang Transform (HHT) for instantaneous frequency tracking.

# \* \*\*Prediction \& Validation\*\*

# &#x20; \* `06\_random\_forest\_prediction.py`: Machine learning decoding of pre-yawning micro-states using Random Forest.

# &#x20; \* `07\_cross\_species\_dtw.py`: Dynamic Time Warping (DTW) for cross-species/cross-state morphological alignment.

# \* \*\*Statistical Modeling (LME \& ANOVA)\*\*

# &#x20; \* `08\_spatial\_dynamics\_lme.py`: Regional EEG power dynamics assessed via Linear Mixed-Effects (LME) models.

# &#x20; \* `9\_regional\_features\_interaction\_lme.py`: Interaction effect analysis (Region × Condition) using Likelihood Ratio Tests (LRT).

# &#x20; \* `10\_figure5\_dhlp\_statistics.py`: Generation of statistical trajectories and Gardner-Altman estimation plots (Fig 5 D, H, L, P).

# &#x20; \* `11\_figure6c\_gamma\_statistics.py`: Quantification of Gamma band energy and volatility.

# &#x20; \* `12\_figure6e\_imf\_volatility.py`: Instantaneous Frequency Volatility of IMF1/IMF2 components.

# \* \*\*Robustness \& Objective Screening\*\*

# &#x20; \* `13\_data\_driven\_time\_window\_scan.py`: Data-driven sliding window scan to prevent P-hacking and identify the optimal EDM epoch.

# &#x20; \* `14\_edm\_occurrence\_quantification.py`: Quantification of EDM occurrence using intra-epoch 75th/25th quartile self-baselines.

# 


# 

# \### 2. `/Docs`

# Contains essential metadata and configuration files.

# \* Includes `.json` dictionaries mapping specific EEG filenames to exact yawn  timestamps (e.g., `eeg\_yawn\_config\_bg3.json`).

# 

# \---

# 

# \## ⚙️ System Requirements \& Dependencies

# 

# The analytical scripts are written in Python. Ensure you have the following key libraries installed:

# 

# ```bash

# pip install numpy pandas scipy scikit-learn statsmodels

# pip install mne        # For EEG data processing

# pip install PyEMD      # For Empirical Mode Decomposition (EMD)

# pip install fastdtw    # For Dynamic Time Warping

# pip install matplotlib seaborn # For publication-quality plotting
