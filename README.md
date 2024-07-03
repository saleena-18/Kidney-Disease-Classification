# Kidney-Disease-Classification

This project is on kidney disease classification using MLflow and DVC. It has been deployed to AWS using GitHub Actions.

## Project Overview

Chronic kidney disease (CKD) is a major public health problem worldwide. Early detection and accurate classification of CKD are crucial for effective treatment and management. This project aims to build a deep learning model to classify the presence of kidney disease using various patient health metrics. The application follows a structured machine learning pipeline with multiple stages for data ingestion, model preparation, training, and evaluation.


## Workflows

1. Update `config.yaml`
2. Update `secrets.yaml`
3. Update `params.yaml`
4. Update the entity
5. Update the configuration manager in `src/config`
6. Update the components
7. Update the pipeline
8. Update `main.py`
9. Update `dvc.yaml`
10. `app.py`

### Steps to Run

1. Clone the repository

    ```bash
    git clone https://github.com/saleena-18/Kidney-Disease-Classification
    ```

2. Create a conda environment

    ```bash
    conda create -n cnncls python=3.10 -y
    conda activate cnncls
    ```

3. Install the requirements

    ```bash
    pip install -r requirements.txt
    ```

4. Finally run the following command

    ```bash
    python app.py
    ```
    
