# Heat Load Forecast 

**Heat Load Forecast** an ML project that predicts heat load using a UCI dataset.

# Getting Started

Install `uv` with:

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Reload your shell:

```bash
source ~/.profile
```

Start the Mlflow UI:

```bash
uv run mlflow ui
```
This starts a local MLflow tracking server at http://127.0.0.1:5000.

Launch Jupyter Lab:

```bash
uv run --with jupyter jupyter lab
```

# Using AWS EC2 and S3 bucket

Follow the instructions in https://github.com/senzhanopt/MLflow-Basic-Demo. 

To run the MLflow server on an EC2 instance with artifacts stored in an S3 bucket, use the following command:
```bash
uv run mlflow server \
    --backend-store-uri sqlite:///~/mlflow_test/mlflow.db \
    --default-artifact-root s3://mlflow-test-bucket/ \
    --host 0.0.0.0 \
    --port 5000 \
    --allowed-hosts "*" \
    --cors-allowed-origins "*"
```
