# Aphasic Discourse Analysis

Date created: November 06, 2025  
Last updated: November 06, 2025

# Project Description
This project provides source code and instructions associated with two Python notebooks for training five classifiers (SVM-rbf, SVM-linear, DT, RF, k-NN) to identify WORD vs NOT WORD and CIU vs NOT CIU (see [Instructions](#instructions)). One notebook provides foundational training and testing with full capture of model performance metrics. The second notebook contains ablation tests and results. Details of each method are described in the associated paper (see [Links](#links)).

# People
**Creator** - Jason M. Pittman<sup>1</sup>  
**Collaborators** - Yesenia Medina-Santos<sup>2</sup> | Anton Phillips Jr<sup>2</sup> | Brie Stark<sup>2</sup>

# Institute
<sup>1</sup> University of Maryland Global Campus USA  
<sup>2</sup> Indiana University Bloomington, Department of Speech, Language and Hearing Sciences USA

# Project Architecture
The operational structure for this project is as follows. Directories not listed are provided based on an internal research template and convenience for future work.

```
.
├── README.md
├── data
├── docs
│   ├── article
│   ├── notes
│   └── presentation
├── src
```

# Instructions
Both notebooks were executed within a Google Colab instance. To reproduce this research, you will need to do the following:

## Drive
1. Create a [Google Drive](https://drive.google.com) account if you do not already have one.
2. In the root of the Drive, created a new directory as `aphasia`.
3. Upload the `aphasia_tokens.csv` from this repo's `data\` directory to the `aphasia` directory in your Drive.

## Colab
1. Launch [Google Colab](https://colab.research.google.com/).
2. Upload the Python notebooks from the `src/` directory in this repo

## Baseline Model Training
The `aphasia_classifiers_trainer.ipynb` contains everything necessary to train and test the five classifier models. When executing the notebook, you will need to grant permissions for Colab to access the Drive account. 

The notebook will output the following:
A. Individual model files will be written to the `aphasia` directory in Drive. Each model has two `.joblib` files: one for WORD and another for CIU.
B. Performance metrics will be written to a ` ` file in Drive. The file will appear as `classifier_metrics_[timestamp].csv`.
C. The same performance metrics will be written to an output cell in the notebook.

## Ablation Tests
The `aphasia_classifiers_ablation.ipynb` contains everything necessary to run ablation tests using the five classifier models. 

The notebook will output the following:
A. Create and write to a `ablation_classic` directory in Drive. 
B. Each model (`.joblib`) will have two sets of files -- WORD and CIU -- while each set will consist of files individual files mapped to each test in the ablation.
C. Test results will be written to `[timestamp]_ablation_metrics.csv`, `[timestamp]_holm_adjustment_CIU.csv`, and `[timestamp]_ablation_stats_vs_baseline.csv`.  


# Links
(Paper)[http://url.com]