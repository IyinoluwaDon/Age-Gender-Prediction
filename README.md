# Chest X-ray Age and Dataset Sex-Class Demo

A Flask demonstration that applies two saved Keras models to an uploaded chest radiograph: one estimates age and one predicts the dataset's binary sex class.

## What is included

- In-memory PNG/JPEG uploads with an 8 MB request limit
- Grayscale, inverted 128 × 128 preprocessing
- Lazy model loading and request/preprocessing regression tests

## Run locally

```sh
python -m venv .venv
# Activate .venv, then:
python -m pip install -r requirements.txt
python app/app.py
```

## Verify

python -m pip install -r requirements-dev.txt
python -m pytest -q

## Repository map

`app/` contains the Flask interface and inference code. `ML_model/` contains the saved models and original notebook. `tests/` covers upload and preprocessing behavior.

## Evidence and limitations

The supplied artifacts can be loaded for inference; automated tests cover request handling and preprocessing, not medical accuracy. Historical notebook metrics are not independently reproduced, and the notebook's evaluation overlaps training data.

Educational reproduction only; not for diagnosis, screening, treatment, employment, insurance or other consequential decisions. The target is a dataset code, not a reliable inference of a person's identity. Dataset and model redistribution rights must be confirmed. No training data is bundled.

## License

No repository license file is included. Unless the project owner adds a license, do not assume the code, data or model artifacts may be redistributed or reused. Verify third-party data and model terms separately.
