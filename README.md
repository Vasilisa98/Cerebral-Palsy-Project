# Cerebral-Palsy-Project

This repository contains all of the step-by-step analyses, simulation inputs, and plots generated for the dissertation on musculoskeletal modeling in children with cerebral palsy.

### code/  
- **step_by_step_analysis.ipynb**  
  Contains the full, annotated Jupyter notebook that walks through every analysis step for the dissertation: from data import, filtering, running OpenSim, through to CEINMS calibration and execution, and plotting the results.  


### Simulation/  
- One folder per participant: six TD subjects  using the **right leg** for simulations, four CP subjects with **right leg** except **PC006** (left leg).  
- **Inside each subject folder** you’ll find:
  - All necessary input files (.c3d file, force-plate data, OpenSim files).  
  - A **ceinms/** subfolder containing the CEINMS setup (EMG mappings, calibration settings, execution scripts).  

- **Plots_for_thesis/** (within each subject):  
  - **All_Activations_plots/** 
  - **All_Moments_plots/**
 
### Notebook Setup

Before running **any** analysis cells in `step_by_step_analysis.ipynb`, you **must** execute the following four sections **in order**:

1. **Imports**  
   Load all required Python packages (e.g. `numpy`, `pandas`, `matplotlib`).  
2. **Class & Function Definitions**  
   Define helper classes (e.g. `Trial`, `OpenSim`) and utility functions for data filtering, file parsing, and plotting.  
3. **Load Participant Data**  
   This section initializes and loads all participant and trial data into the openSim analysis object  
4. **Load Files for the comparison**  
   This cell prepares everything you need to compare CEINMS outputs, static-optimization results, and inverse-dynamics across joints and muscle groups

