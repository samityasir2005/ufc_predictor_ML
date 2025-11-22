# UFC Fight Predictor - PyTorch

Simple neural network for predicting UFC fight outcomes using PyTorch.

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
- **Finish Rates**: KO and submission percentages
- **Experience**: Total fights and rounds

## Model Details

- **Architecture**: 4-layer neural network (64→32→16→1)
- **Accuracy**: ~62-65%
- **Training**: 50 epochs, ~30 seconds on GPU
- **Features**: 19 key statistics
- **Data**: ~10,000 UFC fights with position bias removal

## Example Prediction

```
============================================================
FIGHT PREDICTION
============================================================

Fighter 1: Islam Makhachev (25-1)
  Win Probability: 68.5%

Fighter 2: Charles Oliveira (34-9)
  Win Probability: 31.5%

------------------------------------------------------------
PREDICTED WINNER: Islam Makhachev
Confidence: 68.5%
Assessment: High confidence
============================================================
```

To predict different fighters, edit these lines in the last cell:

```python
fighter1_name = "Your Fighter"
fighter2_name = "Their Fighter"
```


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
- Data augmentation removes position bias (Red vs Blue corner)
- Model saves automatically after training

## Disclaimer

For educational purposes only. Not for betting or financial decisions.
