# Kidney-Disease-Classification

This project demonstrates how to use MLflow and DVC for kidney disease classification. It has been deployed to AWS using GitHub Actions.

## Project Overview

Chronic kidney disease (CKD) is a major public health problem worldwide. Early detection and accurate classification of CKD are crucial for effective treatment and management. This project aims to build a deep learning model to classify the presence of kidney disease using various patient health metrics. The application follows a structured machine learning pipeline with multiple stages for data ingestion, model preparation, training, and evaluation.


## Workflows

1. Update `config.yaml`
2. Update `secrets.yaml` [Optional]
3. Update `params.yaml`
4. Update the entity
5. Update the configuration manager in `src/config`
6. Update the components
7. Update the pipeline
8. Update `main.py`
9. Update `dvc.yaml`
10. `app.py`

## How to Run?

### STEPS:

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

5. Open up your local host and port

## MLflow

To use MLflow for tracking experiments:

1. Run the MLflow UI

    ```bash
    mlflow ui
    ```

2. Set up environment variables for MLflow tracking:

    ```bash
    export MLFLOW_TRACKING_URI=''
    export MLFLOW_TRACKING_USERNAME=''
    export MLFLOW_TRACKING_PASSWORD=''
    ```

3. Run your script:

    ```bash
    python script.py
    ```

## DVC

To use DVC for data version control:

1. Initialize DVC

    ```bash
    dvc init
    ```

2. Reproduce the pipeline

    ```bash
    dvc repro
    ```

3. Visualize the pipeline DAG

    ```bash
    dvc dag
    ```

## About MLflow & DVC

### MLflow

- Production Grade
- Trace all of your experiments
- Logging & tagging your model

### DVC

- Lightweight for POC only
- Lightweight experiments tracker
- Can perform orchestration (creating pipelines)

## AWS CI/CD Deployment with GitHub Actions

### Steps:

1. Login to AWS console.
2. Create IAM user for deployment with specific access:
   - EC2 access: Virtual machine
   - ECR: Elastic Container Registry to save your Docker image in AWS

### Deployment Description:

1. Build Docker image of the source code.
2. Push your Docker image to ECR.
3. Launch your EC2 instance.
4. Pull your image from ECR in EC2.
5. Launch your Docker image in EC2.

### IAM Policy:

1. `AmazonEC2ContainerRegistryFullAccess`
2. `AmazonEC2FullAccess`

### AWS Setup:

1. Create ECR repo to store/save Docker image
   - Save the URI: ` `
2. Create EC2 machine (Ubuntu)
3. Open EC2 and Install Docker in EC2 Machine:

   **Optional:**

```bash
   sudo apt-get update -y
   sudo apt-get upgrade
```

   **Required:**

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker ubuntu
newgrp docker
```

4. Configure EC2 as self-hosted runner:

Settings > Actions > Runner > New self-hosted runner > Choose OS > Then run command one by one

5. Setup GitHub secrets:

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_REGION=us-east-1
AWS_ECR_LOGIN_URI=` `
ECR_REPOSITRY_NAME=mlapp






