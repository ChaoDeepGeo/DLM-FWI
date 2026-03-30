<div align="center">

# DLM-FWI: Deep-Learning-Based Matching for Robust Full-Waveform Inversion

**Your Name**<sup>1</sup> &nbsp;&nbsp;
**Collaborator 1**<sup>2</sup> &nbsp;&nbsp;
**Collaborator 2**<sup>1</sup>

<sup>1</sup> Your Institution  
<sup>2</sup> Collaborator Institution  

![Stars](https://img.shields.io/github/stars/yourname/DLM-FWI?style=social)
![Forks](https://img.shields.io/github/forks/yourname/DLM-FWI?style=social)
![Repo Size](https://img.shields.io/github/repo-size/yourname/DLM-FWI)
![Last Commit](https://img.shields.io/github/last-commit/yourname/DLM-FWI)
![Top Language](https://img.shields.io/github/languages/top/yourname/DLM-FWI)

</div>

---

## Overview

DLM-FWI is a deep-learning-assisted full-waveform inversion framework designed to improve inversion robustness under challenging scenarios such as cycle skipping, limited bandwidth, and inaccurate initial models.  
The method introduces a learned matching strategy to reduce the discrepancy between observed and synthetic seismic data, thereby guiding the inversion toward more reliable subsurface model updates.

---

## Abstract

Full-waveform inversion (FWI) is a powerful technique for high-resolution subsurface model building, but its performance is often limited by cycle skipping, especially when low-frequency information is missing or the initial model is inadequate. To address this issue, we propose **DLM-FWI**, a deep-learning-based matching framework that improves the consistency between observed and predicted seismic data before computing the inversion gradient. By incorporating learned data-domain alignment into the inversion workflow, the proposed method enlarges the convergence basin and enhances inversion stability. Numerical experiments demonstrate that DLM-FWI can recover more accurate large-scale velocity structures than conventional FWI under challenging conditions, indicating its potential for practical seismic imaging applications.

---

## Framework

<p align="center">
  <img src="figures/framework.png" width="850">
</p>

The workflow of DLM-FWI consists of the following main steps:

1. Generate synthetic seismic data from the current velocity model.
2. Use a deep-learning-based matching module to map synthetic data closer to the observed data domain.
3. Compute the misfit between matched synthetic data and observed data.
4. Backpropagate the misfit to update the subsurface model iteratively.

---

## Features

- Robust against cycle skipping
- Improves inversion with poor initial models
- Compatible with conventional FWI workflows
- Supports deep-learning-based data-domain matching
- Easy to extend to acoustic, viscoacoustic, and elastic settings

---

## Installation

To set up the environment, run:

```bash
conda create -n dlmfwi python=3.10
conda activate dlmfwi
pip install numpy scipy matplotlib torch torchvision
pip install jupyter
