# Mesh Based Analysis of Low Fractal Dimension Reinforcement Learning Policies

This directory contains the code to accompany the paper "Mesh Based Analysis of Low Fractal Dimension Reinforcement Learning Policies" submitted to ICRA 2021
This code essentially performs analysis on policies developed in prior work, see: https://github.com/sgillen/fractal_rl

- common.py - Contains functions needed everywhere.
- poincare_mesh_one.ipynb - Takes an rl policy and constructs a poincare mesh
- sT_analysis.ipynb - Takes a mesh file and determines MFPT , eigen values etc.
- validate_mfpt.ipynb - performs monte carlo trials to validate the MFPT
- requirments.txt - Requirements file to install dependencies.


- data17/* results from the variation dimension experiments presented in the prior work
- data_mcshdim4/ results from the mesh dimension experiments presented in the prior work
- data_noise1/ results using the same parameters as data17, but with noise added at training time
- data_noise1_mdim/ results using the same parameters as data_mcshdim4/, but with noise added at training time


Replicating the results requires a mujoco license, we use version 1.51 here. If you have that available you can do the following:

First create a new python environment, in conda this would be:
```
conda create --name corl_repl python=3.6
conda activate corl_repl
```

Then install the requirements in the new environment:
```
pip install -r requirements.txt 
```

To run the jupyter notebook, install the new environment with:
```
python -m ipykernel install --user --name corl_repl
```

From here you should be able to run the notebooks provided to reproduce the figures and tables from the paper.
If you want access the meshes used in the paper they are available on request, but are too large to include in the git repo. Just send an email to sgillen@ucsb.edu

