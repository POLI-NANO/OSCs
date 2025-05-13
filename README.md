# General Machine Learning Models for Interpreting and Predicting Efficiency Degradation in Organic Solar Cells
This repository contains the implementation of the following paper:

**Paper on arxiv:** [2404.00173](https://arxiv.org/abs/2404.00173)

**Paper on SSRN:** [10.2139/ssrn.5147681](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5147681)



## Authors

| Name         | Email address | affiliation  |
|--------------|-----------------|--------------|
|David Valiente|dvaliente@umh.es|University Institute for Engineering Research and Communications Engineering Department, Miguel Hernandez University|
|Fernando Rodríguez-Mas|fernando.rodriguezm@umh.es|Communications Engineering Department, Miguel Hernandez University|
|Juan Vicente Alegre-Requena|jv.alegre@csic.es|Department of Inorganic Chemistry, Institute of Chemical Synthesis and Homogeneous Catalysis (ISQCH), CSIC, University of Zaragoza|
|David Dalmau|ddalmau@unizar.es|Department of Inorganic Chemistry, Institute of Chemical Synthesis and Homogeneous Catalysis (ISQCH), CSIC, University of Zaragoza|
|María Flores|m.flores@umh.es|University Institute for Engineering Research, Miguel Hernandez University|
|Juan Carlos Ferrer|jc.ferrer@umh.es|University Institute for Engineering Research, Miguel Hernandez University|


## Abstract

Photovoltaic (PV) energy plays a key role in addressing the growing global energy demand. Organic solar cells (OSCs) represent a promising alternative to silicon-based PVs due to their low cost, lightweight, and sustainable production. Despite achieving power conversion efficiencies (PCEs) over 20%, OSCs still face challenges in stability and efficiency. Recent advances in manufacturing, artificial intelligence and machine learning (ML) achieve optimized and screened OSCs for greater sustainability and com- mercial viability, thus potentially reducing costs while ensuring stable and long term performance. This work presents optimal ML models to represent the temporal degra- dation on the PCE of polymeric OSCs with structure ITO/PEDOT:PSS/P3HT:PCBM/Al. First, we generated a database with 166 entries with measurements of 5 OSCs, and up to 7 variables regarding the manufacturing and environmental conditions for more than 180 days. Then, we relied on a software framework that provides a conglomer- ation of automated ML protocols that execute sequentially against our database by simply command-line interface. This easily permits hyper-optimizing the ML models through exhaustive benchmarking so that optimal models are obtained. The accuracy for predicting PCE over time reaches values of the coefficient determination widely exceeding 0.90, whereas the root mean squared error, sum of squared error, and mean absolute error are significantly low. Additionally, we assessed the predictive ability of the models using an unseen OSC as an external set. For comparative purposes, classical Bayesian regression fitting are also presented, which only perform sufficiently for univariate cases of single OSCs.


## Datasets 
This repository presents a dataset which consists of PCE measurements of 5 OSC devices. For this dataset, up to 7 variables were registered for more than 180 days.

### Details
Manufacturing variables and environmental conditions at laboratory.

| Variables | Values [min-max] | std | 
|--------------|-------------|------|
|PCE| [0.27-1.32] % | 0.25 |
|quantity DS HTL| [250-1000] μl | 0.19|
|P3HT | [1-1.2] mg | 0.07|
|PCBM | [0.8-1] mg | 0.07|
|ratio P3HT:PCBM | [1-1.25] -| 0.09|
|Temperature | [12-23] °C | 2.81 |
|Hummidity | [33-88] % | 17.78|
|Dew point | [3-19] % | 3.99|
|Pressure | [997-1022] hPa | 7.25|
|Time |  [0-181] days |  60.21|

### Available files
The acquired data are provided in CSV files. 

| Name         | Description | Number of entries |
|--------------|-------------|-------------|
| [data_180_days_all_cells](dataset/data_180_days_all_cells.csv) | all cells   | 166 |
| [data_180_days_no_C4](dataset/data_180_days_no_C4.csv) | without data of cell 4  | 129 |
| [predict_C4_not_seen](dataset/predict_C4_not_seen.csv)| only data of cell 4 | 20 |

The files contains the following header row to indicate the names of the eleven fields provided for each entry:
```
index; PCE; quantity DS HTL; ratio P3HT:PCBM; P3HT; PCBM; temperature; dew point; hummidity; pressure; time
```

## Software

In this work, different ML models are analysed to encode the PCE performance of polymeric OSCs based on ITO/PEDOT:PSS/P3HT:PCBM/Al multilayers. This objective has been achieved by using [ROBERT](https://robert.readthedocs.io/en/latest/index.html). This software framework developed under Python automates data curation, screening of ML models, assessment of predictive ability, and feature analysis. 

For more detailed information about ROBERT program, please refer to https://robert.readthedocs.io/en/latest/index.html

## ROBERT reports

This repository provides the reports obtained with [ROBERT](https://github.com/jvalegre/robert/releases) (v1.0.6) after modeling the entire database.
These are located in the [ROBERT reports](dataset/ROBERT reports) folder of this repository. 

## Citation
If you find this work useful, please consider citing:
```
@misc{valiente_comparing_2025,
	title = {Comparing {Hyper}-optimized {Machine} {Learning} {Models} for {Predicting} {Efficiency} {Degradation} in {Organic} {Solar} {Cells}},
	url = {http://arxiv.org/abs/2404.00173},
	doi = {10.48550/arXiv.2404.00173},
	publisher = {arXiv},
	author = {Valiente, David and Rodríguez-Mas, Fernando and Alegre-Requena, Juan V. and Dalmau, David and Flores, María and Ferrer, Juan C.},
	month = may,
	year = {2025},
}
```
```
@misc{valiente_general_2025,
	title = {General {Machine} {Learning} {Models} for {Interpreting} and {Predicting} {Efficiency} {Degradation} in {Organic} {Solar} {Cells}},
	url = {https://papers.ssrn.com/abstract=5147681},
	doi = {10.2139/ssrn.5147681},
	author = {Valiente, David and Rodríguez-Mas, Fernando and Alegre-Requena, Juan Vicente and Dalmau, David and Flores, María and Ferrer, Juan Carlos},
	month = feb,
	year = {2025},
}
```
