# MO-GPR_data
# README for Ground-Penetrating Radar (GPR) Data Set

## Overview

This repository contains the data and scripts related to the paper titled "A 2D multi-offset and multi-frequency realistic synthetic GPR data set for testing and evaluating processing analysis and inversion routines." The data set includes synthetic GPR data generated using gprMax, detailed descriptions of the acquisition geometry, and the required Conda environment for running the associated Jupyter notebooks.

## Repository Contents

- `env.yml`: Conda environment file listing all dependencies required to run the Jupyter notebooks.
- `notebooks`: Directory containing Jupyter notebooks to open and validate the data files.
- `data`: Directory containing the synthetic GPR data files.

## Data Directory Structure

The `data` directory is organized as follows:

	├── SEGY
	│   ├── 100MHz
	│   │   ├── 100MHz_line0.sgy
	│   │   ├── 100MHz_line1.sgy
	│   │   ├── 100MHz_line2.sgy
	│   │   └── 100MHz_line3.sgy
	│   ├── 200MHz
	│   │   ├── 200MHz_line0.sgy
	│   │   ├── 200MHz_line1.sgy
	│   │   ├── 200MHz_line2.sgy
	│   │   └── 200MHz_line3.sgy
	│   ├── 50MHz
	│   │   ├── 50MHz_line0.sgy
	│   │   ├── 50MHz_line1.sgy
	│   │   ├── 50MHz_line2.sgy
	│   │   └── 50MHz_line3.sgy
	│   └── models
	│       ├── eps
	│       │   ├── line0_eps_25mm.sgy
	│       │   ├── line1_eps_25mm.sgy
	│       │   ├── line2_eps_25mm.sgy
	│       │   └── line3_eps_25mm.sgy
	│       ├── mu
	│       │   ├── line0_mu_25mm.sgy
	│       │   ├── line1_mu_25mm.sgy
	│       │   ├── line2_mu_25mm.sgy
	│       │   └── line3_mu_25mm.sgy
	│       └── sigma
	│           ├── line0_sigm_25mm.sgy
	│           ├── line1_sigm_25mm.sgy
	│           ├── line2_sigm_25mm.sgy
	│           └── line3_sigm_25mm.sgy
	└── wavelets
	    ├── run_100MHz_wave.out
	    ├── run_200MHz_wave.out
	    └── run_50MHz_wave.out
	    

## Setup Instructions

### Conda Environment

1. **Install Conda**: If you do not have Conda installed, you can download it from [Anaconda's official website](https://www.anaconda.com/products/distribution) or [Miniconda's official website](https://docs.conda.io/en/latest/miniconda.html).

2. **Create the Environment**: Navigate to the directory containing the `env.yml` file and run the following command to create the Conda environment:

    ```bash
    conda env create -f env.yml
    ```

3. **Activate the Environment**: Once the environment is created, activate it using:

    ```bash
    conda activate MO_env
    ```

### Jupyter Notebooks

1. **Launch Jupyter Notebook**: With the environment activated, launch Jupyter Notebook by running:

    ```bash
    jupyter notebook
    ```

2. **Open the Notebooks**: Navigate to the `notebooks` directory and open the relevant Jupyter notebooks to explore and validate the data.

## Data Description

### Synthetic GPR Data

The synthetic GPR data set was generated using the gprMax software, which simulates electromagnetic wave propagation using the Finite-Difference Time-Domain (FDTD) method. The data set includes multiple 2D profiles with varying offsets and frequencies, designed to test and evaluate processing, analysis, and inversion routines for GPR data.

### Acquisition Geometry

For each of the four sections selected within the model, 161 shots and 161 receivers were used, covering different frequencies (50 MHz, 100 MHz, and 200 MHz). Detailed sketches and validation methods are provided within the Jupyter notebooks.

## Validation

### Technical Validation

The synthetic data set has been tested to ensure stability and correctness using various commercial and open-source programs, including:

- ProMAX (Halliburton)
- Petrel 17 (Schlumberger)
- Seisee 2.22 (Dalmorneftegeofizika Geophysical Company)
- Prism 2.70.04 (Radar Systems)
- ReflexW 9.5.7 (Sandmaier Geophysical Research)

### Geometry Validation

The acquisition geometry and data readability have been validated by analyzing the stacking chart and comparing common midpoint (CMP) gathers at full-folding cases. Detailed validation results are documented within the Jupyter notebooks.

## Usage Notes

An example Python code to read the header file and additional usage notes can be found within the Jupyter notebooks provided in this repository.

## Contact

For any questions or issues related to this repository, please contact: G. Roncoroni, groncoroni@units.it
