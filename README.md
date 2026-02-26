Predicting Restoration Failures in Primary and Permanent Teeth – A Machine Learning Approach

This repository contains the source code for developing and validating machine learning models to predict posterior dental restoration failures. The code is organized into multiple notebooks, each illustrating different aspects of the data analysis workflow—from data preprocessing and exploratory analysis to model training, hyperparameter tuning, evaluation, and interpretability.

The repository is intended as a reference for researchers and practitioners interested in applying similar techniques to their own datasets. The methods implemented here may be adapted or extended for use in different studies.

Overview

This project demonstrates how to build and evaluate predictive models using advanced machine learning algorithms such as Decision Trees, Random Forests, XGBoost, CatBoost, and Neural Networks. The analytical framework covers:

• Data preprocessing (imputation, scaling, and encoding)

• Cluster-based train-test splitting (to ensure data integrity)

• Model training with cross-validation and nested hyperparameter tuning

• Performance evaluation using accuracy, precision, recall, F1-score, and ROC AUC

• Model interpretability through SHAP analysis

• Calibration assessment of predicted probabilities (calibration slope, CITL, O/E ratio, Brier score, and reliability diagrams)

Repository Structure

• notebooks/ Contains Jupyter/Colab notebooks showcasing the code workflow. The notebooks are grouped as follows:

• Permanent Teeth Analysis (CaCIA)

• CaCIA_ML_FINAL_RESSUBMISSION.ipynb: Comprehensive analysis and modeling for the CaCIA trial dataset.

• Primary Teeth Analysis (CARDEC-3)

• CARDEC_ML_Global_FINAL_RESUBMISSION.ipynb: Analysis of global failures (any type) in the CARDEC-3 trial.

• CARDEC_REPLAC_ML_FINAL_RESUBMISSION.ipynb: Analysis of restoration replacements in the CARDEC-3 trial.

• supplementary/ Contains supplementary material with calibration metrics analysis for all models:

• CaCIA_Calibration.ipynb: Calibration analysis for the CaCIA trial (permanent teeth), including reliability diagrams, calibration slope, calibration-in-the-large (CITL), O/E ratio, and Brier score for all five models.

• CARDEC_Global_Calibration.ipynb: Calibration analysis for the CARDEC-3 trial — any failure (primary teeth).

• CARDEC_Replacement_Calibration.ipynb: Calibration analysis for the CARDEC-3 trial — replacement (primary teeth).

• data/ Contains the datasets used in the analysis:

• AllFinal_CaCIA_Prediction_ML.xlsx: Dataset for the CaCIA trial, including 501 restorations in permanent teeth.

• 2024_corrected_global_CARDEC_3_ML_Vitor.xlsx: Dataset for the CARDEC-3 trial (global analysis), including 637 restorations.

• 2024_corrected_subst_CARDEC_3_ML_Vitor.xlsx: Dataset for the CARDEC-3 trial (replacement analysis), including 637 restorations.

• src/ (Optional) Utility scripts for data preprocessing, model training, and evaluation that can be imported into your own projects.

• requirements.txt Lists the Python dependencies needed to run the notebooks.

Project Description

Analytical Approach

The code demonstrates a comprehensive machine learning pipeline, including:

• Data Splitting: A patient-level train-test split is used to maintain the integrity of the data clusters.

• Preprocessing: Missing values are imputed using appropriate strategies, numerical features are scaled (using z-score normalization), and categorical variables are encoded with one-hot or ordinal encoding methods. Techniques like SMOTE are applied to address class imbalance where needed.

• Model Development: Multiple algorithms are used to build predictive models. Each model is trained with cross-validation, with nested grid search for optimal hyperparameter selection, and evaluated using standard metrics (accuracy, sensitivity, specificity, F1-score, and ROC AUC).

• Interpretability: SHAP analysis is performed to provide insights into the impact of each predictor variable on model outcomes.

• Calibration Assessment: Supplementary notebooks provide a detailed evaluation of the calibration of predicted probabilities for all models, including calibration slope, calibration-in-the-large (CITL), observed/expected (O/E) ratio, Brier score, and reliability diagrams (calibration plots). These metrics assess how well the predicted probabilities correspond to the actual observed event rates.

Adaptability

The shared code is designed to be modular and adaptable. Researchers can use these notebooks as a blueprint to apply similar methodologies to their own studies, adapting the preprocessing steps and modeling strategies to fit different types of clinical or experimental data.

Installation

Clone the Repository:

Set Up a Virtual Environment (optional but recommended):

Install the Dependencies:

Running the Code

• Google Colab: The notebooks are optimized for Google Colab. Open the desired notebook directly in Colab to run the code in an interactive environment.

• Local Execution: Run the notebooks using Jupyter Notebook or JupyterLab:

Reproducibility and Adaptation

The notebooks include detailed comments and documentation outlining the workflow, ensuring that others can follow and adapt the code to their specific needs. While the code illustrates the analytical approach used in our study, it is meant primarily as a reference framework for methodological insights and potential adaptations.

Citation

If you find the code useful for your research, please cite the study as follows:

[It will be updated when published]

Please also reference the trial registration numbers:

• CaCIA Trial: ClinicalTrials.gov (NCT03108586)

• CARDEC 3 Trial: ClinicalTrials.gov (NCT03520309)

Acknowledgements

We thank the research teams and all study participants whose efforts contributed to the development of these analytical methods.

License

MIT License
