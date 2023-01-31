# Identifying Code Changes for Architecture Decay via a Metric Forest Structure

This repository illustrates data and the tool demo video of our TechDebt2023 under-reviewing work —— `Identifying Code Changes for Architecture Decay via a Metric Forest Structure`. The directory is organized as follows.



The whole directory goes like the following:

```
├─README.md
│              
│─Scripts
│	
├─Data         
│  │─Setup
│  │  ├─Subjects
│  │ 
│  └─Results
│     ├─Maintainability Evaluation Results    
│     ├─Architecture Decay Detection Results
|
└─Demo Video 
|
└─Knowledge Base  
│	
├─Scripts
│  ├─Setup
```

## Data

### Setup

This directory contains the preliminary data to conduct the following experiments.

1. #### Subjects


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

This directory contains the demo video of our tool-dbMITPlus.dbMITplus is a web system, developed and implemented based on our dbMIT approach. It aims to localize the cause of software architecture decay by using the metric forest and metric rules.

In this video, LineageOS is used as a case to introduce the four modules of dbMITPlus: Entity and Dependency Extraction, Module Clustering, Architecture Evaluation, Design Problem Detection, and the corresponding visualization.

- **The first module: Entity and Dependency Extraction.** This module extracts syntax dependencies such as method invocation, class inheritance, package import, and historical dependency information such as co-change from source code and commit history.

  When a user inputs basic information of analyzed project , the system  starts the entity and dependency extraction. The system UI will also display the extraction progress. After the progress reaches 100%, the information extraction is completed.

  Users can also view the code package structure of the current software through Project Size TreeMap. TreeMap displays the size of “modules” in a hierarchical structure.

- **The second module: Module Clustering.** Module Clustering reveals the “as-implemented” architecture based on historical dependency.

  The system provides SKM,DBSCAN,SpectralClustering and other clustering algorithms. For example, users can select SKM algorithm for clustering.

- **The third module: Architecture Evaluation.** It evaluates the software maintainability at different granularities with  77 metrics.

  Taking LineageOS as an example, users can observe the project's maintainability level among all projects through the "population distribution" .

  Through the "growth curve" , users can observe the quality changes of 6 versions during the evolution from LineageOS-16.0 to LineageOS-19.1.

  Through the "current profile", users can click on the LineageOS-17.1 to view maintainability measurements of the module in three dimensions.

- **The fourth module: Design Problem Detection.** It pinpoints potential architecture decay causes using a set of pre-defined detection rules. 

  Take LineageOS as an example. In the growth curve of the previous step, LineageOS-16.0 to LineageOS-17.1 experienced a decline in maintainability quality.

  "com.android.server.stats" is the module with the most severe issue. We then detect problematic classes inside this module via class-level metrics of CBC, EDCC, c_FAN OUT. The results suggest that the class "com.android.server.stats.StatsCompanionServicem" frequently invokes the methods across module boundary, leading to a measurement increase. Next, We continue to pinpoint method-level code changes to explain the issue of this class. Method-level maintainability measures indicates that  "StatsCompanionService.pullAppOps" and "StatsCompanionService.pullRoleHolde" are the most severe entities, and each of them depends on more than 10 other modules to implement functionalities. 

  The system can display the information of the two problematic methods that incur heavier maintainability issues.

  Users can employ this information to fix the issue.

## Knowledge Base

## Scripts

### Setup

This directory contains a python script `get_github_projects.py`.It can automatically search microservice systems via Github Restful API.
