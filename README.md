# ML Pipeline Project
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 900">

  <rect width="1200" height="900" fill="#f8f9fa"/>
  
  <!-- Title -->
  <text x="600" y="50" font-family="Arial" font-size="32" text-anchor="middle" font-weight="bold" fill="#333">End-to-End ML Pipeline Workflow</text>
  
  <!-- Stage Boxes -->
  <!-- Data Ingestion -->
  <rect x="100" y="120" width="180" height="100" rx="10" ry="10" fill="#4285f4" fill-opacity="0.8"/>
  <text x="190" y="175" font-family="Arial" font-size="20" text-anchor="middle" fill="white" font-weight="bold">Data Ingestion</text>
  
  <!-- Data Validation -->
  <rect x="360" y="120" width="180" height="100" rx="10" ry="10" fill="#0f9d58" fill-opacity="0.8"/>
  <text x="450" y="175" font-family="Arial" font-size="20" text-anchor="middle" fill="white" font-weight="bold">Data Validation</text>
  
  <!-- Data Transformation -->
  <rect x="620" y="120" width="180" height="100" rx="10" ry="10" fill="#f4b400" fill-opacity="0.8"/>
  <text x="710" y="175" font-family="Arial" font-size="20" text-anchor="middle" fill="white" font-weight="bold">Data Transformation</text>
  
  <!-- Model Trainer -->
  <rect x="880" y="120" width="180" height="100" rx="10" ry="10" fill="#db4437" fill-opacity="0.8"/>
  <text x="970" y="175" font-family="Arial" font-size="20" text-anchor="middle" fill="white" font-weight="bold">Model Trainer</text>
  
  <!-- Model Evaluation -->
  <rect x="620" y="320" width="180" height="100" rx="10" ry="10" fill="#673ab7" fill-opacity="0.8"/>
  <text x="710" y="375" font-family="Arial" font-size="20" text-anchor="middle" fill="white" font-weight="bold">Model Evaluation</text>
  
  <!-- Model Pusher -->
  <rect x="360" y="320" width="180" height="100" rx="10" ry="10" fill="#3f51b5" fill-opacity="0.8"/>
  <text x="450" y="375" font-family="Arial" font-size="20" text-anchor="middle" fill="white" font-weight="bold">Model Pusher</text>
  
  <!-- Deployment -->
  <rect x="100" y="320" width="180" height="100" rx="10" ry="10" fill="#ff5722" fill-opacity="0.8"/>
  <text x="190" y="375" font-family="Arial" font-size="20" text-anchor="middle" fill="white" font-weight="bold">Deployment</text>
  
  <!-- Arrows -->
  <!-- Data Ingestion to Data Validation -->
  <path d="M280 170 L360 170" stroke="#333" stroke-width="3" fill="none" marker-end="url(#arrowhead)"/>
  
  <!-- Data Validation to Data Transformation -->
  <path d="M540 170 L620 170" stroke="#333" stroke-width="3" fill="none" marker-end="url(#arrowhead)"/>
  
  <!-- Data Transformation to Model Trainer -->
  <path d="M800 170 L880 170" stroke="#333" stroke-width="3" fill="none" marker-end="url(#arrowhead)"/>
  
  <!-- Model Trainer to Model Evaluation -->
  <path d="M970 220 L970 270 L800 270 L800 320" stroke="#333" stroke-width="3" fill="none" marker-end="url(#arrowhead)"/>
  
  <!-- Model Evaluation to Model Pusher -->
  <path d="M620 370 L540 370" stroke="#333" stroke-width="3" fill="none" marker-end="url(#arrowhead)"/>
  
  <!-- Model Pusher to Deployment -->
  <path d="M360 370 L280 370" stroke="#333" stroke-width="3" fill="none" marker-end="url(#arrowhead)"/>
  
  <!-- MongoDB -->
  <circle cx="190" cy="520" r="50" fill="#13aa52" fill-opacity="0.8"/>
  <text x="190" y="520" font-family="Arial" font-size="16" text-anchor="middle" fill="white" font-weight="bold">MongoDB</text>
  <text x="190" y="540" font-family="Arial" font-size="12" text-anchor="middle" fill="white">Data Storage</text>
  
  <!-- AWS ECR -->
  <rect x="340" y="480" width="100" height="80" rx="5" ry="5" fill="#ff9900" fill-opacity="0.8"/>
  <text x="390" y="520" font-family="Arial" font-size="16" text-anchor="middle" fill="white" font-weight="bold">AWS ECR</text>
  <text x="390" y="540" font-family="Arial" font-size="12" text-anchor="middle" fill="white">Docker Registry</text>
  
  <!-- AWS EC2 -->
  <rect x="500" y="480" width="100" height="80" rx="5" ry="5" fill="#ff9900" fill-opacity="0.8"/>
  <text x="550" y="520" font-family="Arial" font-size="16" text-anchor="middle" fill="white" font-weight="bold">AWS EC2</text>
  <text x="550" y="540" font-family="Arial" font-size="12" text-anchor="middle" fill="white">Deployment</text>
  
  <!-- GitHub Actions -->
  <rect x="660" y="480" width="100" height="80" rx="5" ry="5" fill="#2088ff" fill-opacity="0.8"/>
  <text x="710" y="520" font-family="Arial" font-size="16" text-anchor="middle" fill="white" font-weight="bold">GitHub</text>
  <text x="710" y="540" font-family="Arial" font-size="12" text-anchor="middle" fill="white">CI/CD Pipeline</text>
  
  <!-- Data Ingestion Details -->
  <rect x="100" y="620" width="250" height="150" rx="5" ry="5" fill="#e3f2fd" stroke="#4285f4" stroke-width="2"/>
  <text x="225" y="640" font-family="Arial" font-size="16" text-anchor="middle" font-weight="bold" fill="#4285f4">Data Ingestion</text>
  <text x="110" y="665" font-family="Arial" font-size="12" fill="#333">• Read from MongoDB</text>
  <text x="110" y="685" font-family="Arial" font-size="12" fill="#333">• Configure paths and split ratio</text>
  <text x="110" y="705" font-family="Arial" font-size="12" fill="#333">• Split into train/test datasets</text>
  <text x="110" y="725" font-family="Arial" font-size="12" fill="#333">• Create Feature Store (CSV)</text>
  <text x="110" y="745" font-family="Arial" font-size="12" fill="#333">• Generate timestamped artifacts</text>
  
  <!-- Data Validation Details -->
  <rect x="370" y="620" width="250" height="150" rx="5" ry="5" fill="#e8f5e9" stroke="#0f9d58" stroke-width="2"/>
  <text x="495" y="640" font-family="Arial" font-size="16" text-anchor="middle" font-weight="bold" fill="#0f9d58">Data Validation</text>
  <text x="380" y="665" font-family="Arial" font-size="12" fill="#333">• Schema validation</text>
  <text x="380" y="685" font-family="Arial" font-size="12" fill="#333">• Column count verification</text>
  <text x="380" y="705" font-family="Arial" font-size="12" fill="#333">• Numerical column existence check</text>
  <text x="380" y="725" font-family="Arial" font-size="12" fill="#333">• Data drift detection</text>
  <text x="380" y="745" font-family="Arial" font-size="12" fill="#333">• Generate validation report</text>
  
  <!-- Data Transformation Details -->
  <rect x="640" y="620" width="250" height="150" rx="5" ry="5" fill="#fff8e1" stroke="#f4b400" stroke-width="2"/>
  <text x="765" y="640" font-family="Arial" font-size="16" text-anchor="middle" font-weight="bold" fill="#f4b400">Data Transformation</text>
  <text x="650" y="665" font-family="Arial" font-size="12" fill="#333">• Robust scaling</text>
  <text x="650" y="685" font-family="Arial" font-size="12" fill="#333">• Missing value imputation</text>
  <text x="650" y="705" font-family="Arial" font-size="12" fill="#333">• Feature engineering</text>
  <text x="650" y="725" font-family="Arial" font-size="12" fill="#333">• SMOTE/Tomek for imbalanced data</text>
  <text x="650" y="745" font-family="Arial" font-size="12" fill="#333">• Save as numpy arrays</text>
  
  <!-- Model Training & Evaluation Details -->
  <rect x="910" y="620" width="250" height="150" rx="5" ry="5" fill="#fbe9e7" stroke="#db4437" stroke-width="2"/>
  <text x="1035" y="640" font-family="Arial" font-size="16" text-anchor="middle" font-weight="bold" fill="#db4437">Model Training & Evaluation</text>
  <text x="920" y="665" font-family="Arial" font-size="12" fill="#333">• Load numpy arrays</text>
  <text x="920" y="685" font-family="Arial" font-size="12" fill="#333">• Model selection via Model Factory</text>
  <text x="920" y="705" font-family="Arial" font-size="12" fill="#333">• Neural Data Model training</text>
  <text x="920" y="725" font-family="Arial" font-size="12" fill="#333">• Metric calculation and evaluation</text>
  <text x="920" y="745" font-family="Arial" font-size="12" fill="#333">• Model acceptance/rejection</text>
  
  <!-- MongoDB to Data Ingestion connection -->
  <path d="M190 470 L190 420" stroke="#13aa52" stroke-width="2" stroke-dasharray="5,5" fill="none" marker-end="url(#arrowhead)"/>
  
  <!-- Deployment to AWS ECR connection -->
  <path d="M190 420 L190 460 L340 520" stroke="#ff9900" stroke-width="2" stroke-dasharray="5,5" fill="none" marker-end="url(#arrowhead)"/>
  
  <!-- AWS ECR to AWS EC2 connection -->
  <path d="M440 520 L500 520" stroke="#ff9900" stroke-width="2" stroke-dasharray="5,5" fill="none" marker-end="url(#arrowhead)"/>
  
  <!-- GitHub to Deployment connection -->
  <path d="M660 520 L600 520 L550 450 L280 450 L190 420" stroke="#2088ff" stroke-width="2" stroke-dasharray="5,5" fill="none" marker-end="url(#arrowhead)"/>
  
  <!-- Arrowhead marker definition -->
  <defs>
    <marker id="arrowhead" markerWidth="10" markerHeight="7" refX="9" refY="3.5" orient="auto">
      <polygon points="0 0, 10 3.5, 0 7" fill="#333"/>
    </marker>
  </defs>
</svg>

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
