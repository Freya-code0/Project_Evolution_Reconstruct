# Introduction

This directory contains the code of link prediction task for paper ''Restore structure evolution trajectory of networked complex systems.'' 


# Usage

### Installation

## `weightedlinkprediction` package
The link prediction task is implemented as a Python package `weightedlinkprediction`. We recommend installing the package locally. To do so, go to the directory `code_link_prediction`, make sure your virtual environment for this project is activated, then run

```bash
pip install -e ./
```

Then you can try

```python
import weightedlinkprediction.utils
import weightedlinkprediction.adamic_adar_predict
```
to check whether the package is installed properly.

### Requirements
The code is implemented with Python 3.9.15. The following packages are required:
```bash
scipy==1.9.0
networkx==2.8.5
numpy==1.23.1
```

### Demos

Please check out the demo workflows under `code_link_prediction/xx_link_prediction`.
We use [`snakemake`](https://snakemake.readthedocs.io/en/stable/) to organize our workflows.

For example, you can run 
```python
snakemake run_tsvd_repeat_all -j1
```
in folder `code_link_prediction/tsvd_link_prediction` to get the link prediction result of the example network `worm` using TSVD (Truncated Singular Value Decomposition) algorithm with parameter `\theta = 0.1` and `truncated_k = 5`.

**[Note]**: The input edge sequence data and output data both stored in folder `public_code_data_figures/data`.


### SPM link prediticon
if you want to run this file, you need run it in the fold "code_machine_learning"  and you should run the code" _GetLpSort_CPNN.py" first.