# ML Pipeline Project

## Project Overview
This project implements a complete end-to-end machine learning pipeline following MLOps best practices. The pipeline handles every stage from data collection to model deployment in production, with emphasis on automation, validation, and monitoring.

## Architecture
The system is designed as a modular pipeline with the following components:

1. **Data Ingestion**: Pulls data from MongoDB, prepares datasets, and splits into training and testing sets
2. **Data Validation**: Validates data quality, schema consistency, and detects drift
3. **Data Transformation**: Preprocesses data with feature engineering, scaling, and imbalance handling
4. **Model Trainer**: Trains multiple models through a model factory and selects the best performer
5. **Model Evaluation**: Evaluates model performance against defined metrics and acceptance criteria
6. **Model Pusher**: Moves accepted models to production environment
7. **Deployment**: Deploys models to AWS using Docker containers and CI/CD automation

## Tech Stack
- **Database**: MongoDB
- **Processing**: Python, NumPy, scikit-learn
- **Deployment**: Docker, AWS ECR, AWS EC2
- **CI/CD**: GitHub Actions
- **ML Techniques**: RNN Imputer, SMOTE/Tomek for imbalanced data, Neural Data Models

## Pipeline Stages

### 1. Data Ingestion
- **Input**: Raw data from MongoDB
- **Operations**:
  - Configure data paths and parameters
  - Split data into train/test sets
  - Create Feature Store in CSV format
  - Generate timestamped artifacts
- **Output**: train.csv and test.csv files

### 2. Data Validation
- **Input**: train.csv and test.csv
- **Operations**:
  - Schema validation
  - Column count verification
  - Numerical column existence check
  - Data drift detection
  - Validation reporting
- **Output**: Validation report with pass/fail status

### 3. Data Transformation
- **Input**: Validated datasets
- **Operations**:
  - Robust scaling
  - Missing value imputation
  - Feature engineering
  - SMOTE/Tomek handling for imbalanced data
  - Array conversion
- **Output**: train.npy and test.npy files with preprocessing.pkl

### 4. Model Trainer
- **Input**: Transformed data arrays
- **Operations**:
  - Data loading and splitting
  - Model training through Model Factory
  - Neural Data Model creation
  - Best model selection based on metrics
  - Model serialization
- **Output**: model.pkl file

### 5. Model Evaluation
- **Input**: Trained model and test data
- **Operations**:
  - Performance metric calculation
  - Comparison against acceptance criteria
  - Accept/reject decision
- **Output**: Evaluation report and acceptance status

### 6. Model Pusher
- **Input**: Accepted model
- **Operations**:
  - Model preparation for production
  - Artifact generation
- **Output**: Production-ready model

### 7. Deployment
- **Input**: Production model
- **Operations**:
  - Docker image creation
  - Security configuration
  - AWS ECR image push
  - EC2 deployment via GitHub Actions
- **Output**: Running model in production environment

## Setup Instructions

### Prerequisites
- Python 3.8+
- Docker
- AWS Account with ECR and EC2 access
- MongoDB instance

### Installation
1. Clone the repository
```bash
git clone https://github.com/yourusername/ml-pipeline-project.git
cd ml-pipeline-project
```

2. Install dependencies
```bash
pip install -r requirements.txt
```

3. Configure environment variables
```bash
# Create .env file with necessary configuration
# Example:
MONGODB_URI=mongodb://localhost:27017
AWS_ACCESS_KEY_ID=your_access_key
AWS_SECRET_ACCESS_KEY=your_secret_key
AWS_REGION=us-west-2
```

4. Run the pipeline locally
```bash
python run_pipeline.py
```

### Deployment
1. Configure AWS credentials and Docker
2. Push to GitHub to trigger CI/CD pipeline
3. Monitor deployment in GitHub Actions

## Project Structure
```
ml-pipeline-project/
│
├── config/                   # Configuration files
│   ├── data_ingestion_config.py
│   ├── data_validation_config.py
│   ├── data_transformation_config.py
│   ├── model_trainer_config.py
│   ├── model_evaluation_config.py
│   └── model_pusher_config.py
│
├── components/               # Pipeline components
│   ├── data_ingestion.py
│   ├── data_validation.py
│   ├── data_transformation.py
│   ├── model_trainer.py
│   ├── model_evaluation.py
│   └── model_pusher.py
│
├── entity/                   # Data entities and structures
│   ├── artifact_entity.py
│   └── config_entity.py
│
├── constants/                # Constants and configurations
│
├── pipeline/                 # Pipeline orchestration
│   ├── training_pipeline.py
│   └── prediction_pipeline.py
│
├── utils/                    # Utility functions
│
├── templates/                # HTML/UI templates if applicable
│
├── static/                   # Static assets
│
├── logs/                     # Log files
│
├── artifacts/                # Generated artifacts
│
├── tests/                    # Test cases
│
├── .github/                  # GitHub Actions workflows
│   └── workflows/
│       └── deploy.yml
│
├── Dockerfile                # Docker configuration
├── docker-compose.yml        # Docker compose configuration
├── requirements.txt          # Python dependencies
├── setup.py                  # Package setup
├── .gitignore
└── README.md
```

## Contributing
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## License
This project is licensed under the MIT License - see the LICENSE file for details
