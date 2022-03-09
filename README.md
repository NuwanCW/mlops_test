## This is only for testing mlops please do not use
## Packaging with venv
```bash
python3 -m venv venv
source venv/bin/activate
python -m pip install --upgrade pip setuptools wheel
python -m pip install -e ".[dev]"
```

## Organization
```bash
config/
├── config.py        - configuration setup
├── params.json      - training parameters
└── test_params.py   - training test parameters
tagifai/
├── data.py          - data processing components
├── eval.py          - evaluation components
├── main.py          - training/optimization pipelines
├── models.py        - model architectures
├── predict.py       - inference components
├── train.py         - training components
└── utils.py         - supplementary utilities
```

## Operations
```python linenums="1"
from pathlib import Path
from config import config
from tagifai import main

# Load data
main.load_data()

# Compute features
main.compute_features()
MLops testing
