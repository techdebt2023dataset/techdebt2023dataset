# Identifying Code Changes for Architecture Decay via a Metric Forest Structure

This repository illustrates data and the tool demo video of our TechDebt2023 under-reviewing work —— `Identifying Code Changes for Architecture Decay via a Metric Forest Structure`. The directory is organized as follows.



The whole directory goes like the following:

[TOC]

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
- **The second module: Module Clustering.** Module Clustering reveals the “as-implemented” architecture based on historical dependency.
- **The third module: Architecture Evaluation.** It evaluates the software maintainability at different granularities with  77 metrics.
- **The fourth module: Design Problem Detection.** It pinpoints potential architecture decay causes using a set of pre-defined detection rules. 

## Knowledge Base

## Scripts

### Setup

This directory contains a python script `get_github_projects.py`.It can automatically search microservice systems via Github Restful API.
