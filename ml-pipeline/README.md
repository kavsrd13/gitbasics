# ML Pipeline

This repository contains an end-to-end machine learning pipeline.

## Files

- `train.py`: Script for training the model.
- `config.yaml`: Configuration file for hyperparameters and paths.
- `requirements.txt`: List of dependencies.

## Usage

1. **Install dependencies**
    ```bash
    pip install -r requirements.txt
    ```

2. **Configure parameters**
    - Edit `config.yaml` to set dataset paths, model parameters, and training options.

3. **Train the model**
    ```bash
    python train.py --config config.yaml
    ```

## Configuration

Sample `config.yaml`:
```yaml
data:
  train_path: "data/train.csv"
  test_path: "data/test.csv"
model:
  type: "RandomForest"
  parameters:
     n_estimators: 100
     max_depth: 10
training:
  epochs: 20
  batch_size: 32
output:
  model_path: "models/model.pkl"
```

## Requirements

Sample `requirements.txt`:
```
numpy
pandas
scikit-learn
pyyaml
```

## train.py Overview

- Loads configuration from `config.yaml`
- Preprocesses data
- Trains the model
- Saves the trained model to the specified path

## License

MIT