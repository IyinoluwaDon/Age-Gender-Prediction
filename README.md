# Chest X-ray Age and Dataset Sex-Class Models

Flask inference application for two separately trained Keras deep convolutional neural networks that analyze chest radiographs: an age estimator and a classifier for the dataset's binary sex label. The application serves the models; the saved weights and original training notebook are in `ML_model/`.

The notebook joins a Kaggle-style image directory with `train_age.csv` and `train_gender.csv`, converts images to grayscale, inverts pixel values, and resizes them to 128 x 128. The gender network is a sigmoid binary classifier trained with Adam and binary cross-entropy; the age network uses a linear output trained with Adam and mean-squared error. The Flask app applies the same preprocessing to in-memory PNG/JPEG uploads and loads each model on demand. `tests/` covers upload and preprocessing behavior.

## Run locally

```sh
python -m venv .venv
# Activate .venv, then:
python -m pip install -r requirements.txt
python app/app.py
```

See `ML_model/` for the training notebook and model artifacts and `requirements-dev.txt` for the test dependencies.
