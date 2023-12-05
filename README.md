# Machine-Learning-with-Vertex-AI-on-Google-Cloud

## Overview

This repository contains code and resources related to machine learning using Google Cloud's Vertex AI. The project leverages BigQuery for data collection and preprocessing before building machine learning models with Vertex AI.

## Contents

- **`src/`**: This directory contains the source code for various machine learning models and utilities.
- **`data/`**: You can store your training and testing datasets in this directory.
- **`notebooks/`**: Jupyter notebooks showcasing examples and tutorials for using Vertex AI and BigQuery.
- **`docs/`**: Documentation files explaining the project structure, setup, and usage.

## Getting Started

### Prerequisites

Before running the code, make sure you have the following installed:

- Python (version 3.10.8)
- Google Cloud SDK
- Additional dependencies (list them, if any)

### Setup

1. Clone this repository:

   ```bash
   git clone https://github.com/pradeep-016/Machine-Learning-with-Vertex-AI-on-Google-Cloud.git
   cd Machine-Learning-with-Vertex-AI-on-Google-Cloud
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Configure Google Cloud credentials:

   ```bash
   gcloud auth application-default login
   ```

4. Additional setup steps, if any.

### Using BigQuery for Data Collection

1. Create a BigQuery dataset and table for your project.

2. Use the following command to export data from BigQuery to a CSV file:

   ```bash
   bq extract --destination_format CSV your-project:your-dataset.your-table data/train.csv
   ```

   Replace `your-project`, `your-dataset`, and `your-table` with your actual values.

### Using Vertex AI for Model Training

1. Upload your dataset to Google Cloud Storage:

   ```bash
   gsutil cp data/train.csv gs://your-bucket/data/train.csv
   ```

   Replace `your-bucket` with your actual bucket name.

2. Run the following command to train a model using Vertex AI:

   ```bash
   python src/train_model.py --input gs://your-bucket/data/train.csv --output gs://your-bucket/models/model.pkl
   ```

   Update the input and output paths accordingly.

