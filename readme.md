# Identifying Code Changes for Architecture Decay via a Metric Forest Structure

This repository illustrates data and the tool demo video of our TechDebt2023 under-reviewing work —— `Identifying Code Changes for Architecture Decay via a Metric Forest Structure`. The directory is organized as follows.



The whole directory goes like the following:

```
├─README.md 
│	
├─Data     
│  │─Setup
│  │    ├─Subjects
│  └─Results
│     ├─Maintainability Evaluation Results    
│     ├─Architecture Decay Detection Results
|
└─Demo video      
|
└─Scripts 
│  │─Setup
```

  

## Data

### Setup

This directory contains the preliminary data to conduct the following experiments.

#### Subjects

This directory contains information about all projects mentioned in the paper. It includes loc and the number of files, commits, modules, classes, methods of the project (the latest version is obtained for all multi-version projects).

### Results

This directory contains all experimental results.

#### Maintainability Evaluation Results

This directory contains the file of evaluation results. The SCORE and DL values of 65 projects are counted in the file.

#### Architecture Decay Detection Results

This directory contains two files: `detection results.xlsx` and `maintenance cost.xlsx`.

- **detection results.xlsx**: This file contains statistical number of all root causes entities.
- **maintenance cost.xlsx**: This file contains the maintenance cost of 6 projects.

## Demo Video

This directory contains the demo video of our tool-dbMITPlus.

## Scripts

### Setup

This directory contains a python script `get_github_projects.py`.It can automatically search microservice systems via Github Restful API.
