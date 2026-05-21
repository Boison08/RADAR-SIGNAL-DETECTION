# Micro-Doppler Spectrogram Classifier

Prototype repository for radar-signal classification using a CNN trained on I/Q-derived spectrograms.

## Structure

- `micro_doppler_classifier.ipynb` — exploratory notebook (data gen, training, evaluation).
- `radar_signal_classification.ipynb` — additional notebook (if present).
- `src/` — core Python modules and training scripts.
  - `src/model.py` — model definition (`MicroDopplerCNN`).
  - `src/dataset.py` — dataset helpers for spectrogram arrays.
  - `src/train.py` — CLI training script.
- `requirements.txt` — Python dependencies.
- `.gitignore` — common ignores for Python projects.

## Quick start

1. Create a virtual environment (recommended):

```bash
python -m venv .venv
# On Windows
.venv\Scripts\activate
# On macOS / Linux
source .venv/bin/activate
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Generate data using the notebook `micro_doppler_classifier.ipynb` (or save arrays `X.npy` and `y.npy`).

4. Train from saved numpy arrays:

```bash
python src/train.py --X data/X.npy --y data/y.npy --epochs 20 --batch-size 32
```

## Notes
- This repo contains a compact, beginner-friendly CNN suitable for prototyping. For production, consider transfer learning, quantization, and edge acceleration.
- See the notebooks for data generation, visualization, and evaluation examples.

## License
Add a license if you plan to publish this repository.
