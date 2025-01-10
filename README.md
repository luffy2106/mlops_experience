# MLOPS_experience

## Setup environment

To ensure there is no conflict in term of dependency, it is recommened to use **Poetry** as Python dependency management framework.

1. Install dependencies

If your project already has a `pyproject.toml` file, install the dependencies by running:

```bash
poetry install
```

2. Activate the virtual environment

```bash
poetry shell
```

3. Manage dependencies

* To add a package

```bash
poetry add package_name
```

* To remove a package

```bash
poetry remove package_name
```

* To update dependencies

```bash
poetry update 
```

## Training

Take a look at mlops_experience/notebooks/text_classification_mlflow.ipynb to see how to train and track the model performance with mlflows

### Setup

To be able to tracking the training model in real time, you need to ensure that you start the MLflow server first.

```bash
mlflow server --host 0.0.0.0 --port 5000
```

Then you can run the training script in text_classification_mlflow.ipynb

To track the training model, you need to access mlflow

```bash
mlflow ui
```


By default, MLflow saves logs to the `./mlruns` directory in your working directory. With a tracking server running, it saves to:

* Data: `./mlruns` (local) or configured database
* Artifacts: `./mlruns` or configured artifact store (S3, Azure Blob, etc.)

### Performance tracking in MLflow UI
