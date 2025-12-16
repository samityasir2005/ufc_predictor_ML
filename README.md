# UFC Fight Predictor - PyTorch

Simple Machine learning model for predicting UFC fight outcomes using PyTorch.

## Quick Start

### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

### 2. Run in Google Colab (Recommended)

1. Upload `notebooks/ufc_pytorch_predictor.ipynb` to [Google Colab](https://colab.research.google.com/)
2. Go to `Runtime` → `Change runtime type` → Select **GPU**
3. Run all cells: `Runtime` → `Run all`
4. Edit fighter names in the last cell to predict custom matchups

### 3. Or Run Locally

Open and run `notebooks/ufc_pytorch_predictor.ipynb` in Jupyter/VS Code.

## What It Does

The model analyzes 19 fighter statistics to predict who will win:

- **Physical**: Height, reach, age
- **Record**: Wins, losses, win rates
- **Momentum**: Win/loss streaks
- **Fighting Stats**: Striking, takedowns, submissions


## Model Details

- **Architecture**: 4-layer neural network (64→32→16→1)
- **Accuracy**: ~60%
- **Training**: 50 epochs, ~30 seconds on GPU
- **Features**: 19 key statistics
- **Data**: ~7,000 UFC fights with position bias removal


## Requirements

- Python 3.7+
- PyTorch
- pandas, numpy
- scikit-learn
- matplotlib, seaborn
- kagglehub

See `requirements.txt` for exact versions.

## Dataset

Uses the [Ultimate UFC Dataset](https://www.kaggle.com/datasets/mdabbert/ultimate-ufc-dataset) from Kaggle.

## Notes

- Best run on Google Colab with GPU for faster training
- Betting odds and outcome columns are removed to prevent data leakage

## Disclaimer

For educational purposes only. Not for betting or financial decisions.
