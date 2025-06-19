# DRIFTS-analysis
## Description
NOTE: active version is now on GitLab (https://git.science.uu.nl/icc-coders/drifts-analysis-package). This version will not be kept up-to-date.

This repository contains my DRIFTS_package. Among others, the package can be used to import .dx files, logfiles and GC data from various IR setups from Bruker.

## Installation 
- clone the repository:
```
git clone https://github.com/Hojano/DRIFTS-analysis
```
- install the package by **navigating to the cloned repository** in your python environment and executing the following command:

```
pip install -r requirements.txt
pip install -e .
```
- You should now be able to load the package in python by using:

```python
import DRIFTS_package as ir
```

## Installation (simplest version, not recommended)
- Download the repository. 
- Copy the *DRIFTS_package* folder to the folder where the script you wanna use for analysis is located. Example:

```
My_Scripts
│
└───DRIFTS
│   │   myDRIFTS_analysis.py
│   │   myDRIFTS_notebook.ipynb
│   │
│   └───*DRIFTS_package*
```

## Usage
Parse DRIFTS files from a folder using:
```python
DRIFTS_spectra = ir.parse_spectra('*path-to-your-file*')
```
Make a quick plot to check: 

```python
ir.quick_plot(DRIFTS_spectra)
```
Combine with logfile:

```python
merged_data = ir.merge_spectra_logfile('*path to spectra*', '*path to logfile*')
```

Check the example notebook for more info how to use this package.

## Support
If you find bugs or have other questions send me a message or open an issue.

## Contributing
If you want to contribute, let me know.

## Authors
Jan den Hollander, Utrecht University

## Acknowledgements
Package structure was adapted from pyTGA, built by Sebastian Rejman
