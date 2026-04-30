# Breast Cancer Classifier

Machine learning pipeline for breast cancer classification. Covers the full ML lifecycle: data loading, preprocessing, feature engineering, model training, and evaluation. Served via a Flask REST API.

## Dependencies

| Dependency | Version |
|---|---|
| Python | >= 3.12 |
| TensorFlow | >= 2.21.0 |
| scikit-learn | >= 1.8.0 |
| pandas | >= 3.0.2 |
| numpy | >= 2.4.4 |
| Flask | >= 3.1.3 |
| gunicorn | >= 25.3.0 |
| PyYAML | >= 6.0.3 |

## Installation

**Requirements:** [uv](https://docs.astral.sh/uv/) must be installed.

```bash
# Clone the repo
git clone https://github.com/felipe-mizidorio/breast_cancer_classifier.git
cd breast_cancer_classifier

# Install dependencies
uv sync

# Install with dev dependencies
uv sync --group dev
```

### Docker

```bash
docker build -t breast-cancer-classifier .
docker run -p 8000:8000 breast-cancer-classifier
```

## Usage

```bash
# Run via uv
uv run breast-cancer-classifier

# Or activate the virtual environment first
source .venv/bin/activate
breast-cancer-classifier
```

## Project Structure

```
breast_cancer_classifier/
├── src/
│   └── breast_cancer_classifier/
│       ├── data_loading/          # Dataset ingestion
│       ├── data_preprocessing/    # Cleaning and normalization
│       ├── feature_engineering/   # Feature extraction and selection
│       ├── model_training/        # Model definition and training
│       └── model_evaluation/      # Metrics and validation
├── data/
│   ├── raw/                       # Original unmodified data
│   ├── preprocessed/              # Intermediate processed data
│   └── processed/                 # Final data ready for training
├── models/                        # Saved trained models
├── metrics/                       # Evaluation outputs
├── artifacts/                     # Misc training artifacts
├── params.yaml                    # Pipeline hyperparameters
├── pyproject.toml                 # Project metadata and dependencies
└── Dockerfile                     # Container definition
```
