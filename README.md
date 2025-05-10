# General Machine Learning Models for Interpreting and Predicting Efficiency Degradation in Organic Solar Cells
This repository contains the implementation of the following paper:

**Paper on arxiv:** [2404.00173](https://arxiv.org/abs/2404.00173)

**Paper on SSRN:** [10.2139/ssrn.5147681](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5147681)



## Authors

| Name         | Email addresses | affiliation  |
|--------------|-----------------|--------------|
|David Valiente|dvaliente@umh.es|University Institute for Engineering Research and Communications Engineering Department, Miguel Hernandez University|
|Fernando Rodríguez-Mas|fernando.rodriguezm@umh.es|Communications Engineering Department, Miguel Hernandez University|
|Juan Vicente Alegre-Requena|jv.alegre@csic.es|Department of Inorganic Chemistry, Institute of Chemical Synthesis and Homogeneous Catalysis (ISQCH), CSIC, 
  University of Zaragoza|
|David Dalmau|ddalmau@unizar.es|Department of Inorganic Chemistry, Institute of Chemical Synthesis and Homogeneous Catalysis (ISQCH), CSIC, 
  University of Zaragoza|
|María Flores|m.flores@umh.es|University Institute for Engineering Research, Miguel Hernandez University|
|Juan Carlos Ferrer|jc.ferrer@umh.es|University Institute for Engineering Research, Miguel Hernandez University|


## Abstract

Photovoltaic (PV) energy plays a key role in addressing the growing global energy demand. Organic solar cells (OSCs) represent a promising alternative to silicon-based PVs due to their low cost, lightweight, and sustainable production. Despite achieving power conversion efficiencies (PCEs) over 20%, OSCs still face challenges in stability and efficiency. Recent advances in manufacturing, artificial intelligence and machine learning (ML) achieve optimized and screened OSCs for greater sustainability and com- mercial viability, thus potentially reducing costs while ensuring stable and long term performance. This work presents optimal ML models to represent the temporal degra- dation on the PCE of polymeric OSCs with structure ITO/PEDOT:PSS/P3HT:PCBM/Al. First, we generated a database with 166 entries with measurements of 5 OSCs, and up to 7 variables regarding the manufacturing and environmental conditions for more than 180 days. Then, we relied on a software framework that provides a conglomer- ation of automated ML protocols that execute sequentially against our database by simply command-line interface. This easily permits hyper-optimizing the ML models through exhaustive benchmarking so that optimal models are obtained. The accuracy for predicting PCE over time reaches values of the coefficient determination widely exceeding 0.90, whereas the root mean squared error, sum of squared error, and mean absolute error are significantly low. Additionally, we assessed the predictive ability of the models using an unseen OSC as an external set. For comparative purposes, classical Bayesian regression fitting are also presented, which only perform sufficiently for univariate cases of single OSCs.


## Datasets 
This repository presents a dataset which consists of PCE measurements of 5 OSC devices. For this dataset, up to 7 variables were registered for more than 180 days.

| Name         | Description |
|--------------|-------------|
| [data_180_days_all_cells](dataset/data_180_days_all_cells.csv) | Celda 1,2   |
| [data_180_days_no_C4](dataset/data_180_days_no_C4.csv) | Celda 2,2   |
| [predict_C4_not_seen](dataset/predict_C4_not_seen.csv)| Celda 2,2   |


## Software

In this work, different ML models are analysed to encode the PCE performance of polymeric OSCs based on ITO/PEDOT:PSS/P3HT:PCBM/Al multilayers. [ROBERT](https://github.com/jvalegre/robert/releases) (v1.0.6)

Documentation about ROBERT program can be found at https://robert.readthedocs.io/en/latest/index.html

## ROBERT reports
ROBERT 


## Citation
If you find this work useful, please consider citing:
```
@misc{valiente2025comparinghyperoptimizedmachinelearning,
      title={Comparing Hyper-optimized Machine Learning Models for Predicting Efficiency Degradation in Organic Solar Cells}, 
      author={David Valiente and Fernando Rodríguez-Mas and Juan V. Alegre-Requena and David Dalmau and María Flores and Juan C. Ferrer},
      year={2025},
      eprint={2404.00173},
      archivePrefix={arXiv},
      primaryClass={cs.LG},
      url={https://arxiv.org/abs/2404.00173}, 
}
```

