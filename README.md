# BTC LSTM Trading Project

This repository contains an MSc-level cryptocurrency forecasting and algorithmic trading project built around Bitcoin (BTC-USD). The core work is centered on a multivariate LSTM forecasting model, feature engineering, backtesting with Backtrader, and robustness analysis using search and walk-forward techniques.

## Repository Contents

- `notebooks/BTC_LSTM.ipynb` - primary notebook with data download, preprocessing, LSTM model training, evaluation, trading strategy simulation, and post-hoc analyses.
- `notebooks/BERT_BTC_LSTM.ipynb` - supplemental notebook exploring an NLP-enhanced model variant using BERT-related features.
- `Trading_Eval.ipynb` - evaluation notebook for analyzing model and trading results.
- `requirements.txt` - pinned Python dependencies required to reproduce the project.
- `MSc_Project_Report_v1.pdf` - MSc project report describing methodology, experiments, and findings.
- `best_model.pt` - saved PyTorch model weights from the main training run.
- `decision_log.csv`, `trade_log.csv`, `equity_curves.csv`, `random_search_results.csv`, `walk_forward_results.csv` - generated analysis outputs from backtest and optimization workflows.
- `docs/` and `archive/` - placeholder directories for documentation and archived materials.

## Setup

1. Create and activate a virtual environment:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Upgrade pip and install dependencies:

```powershell
python -m pip install --upgrade pip
pip install -r requirements.txt
```

3. Open the notebook files in Jupyter Notebook or VS Code and execute the cells in order.

## Usage

- Start with `notebooks/BTC_LSTM.ipynb` for the main workflow: data acquisition, feature engineering, model training, testing, and trading simulation.
- If the notebook already includes saved outputs, you can re-run only the relevant cells to refresh charts and metrics.
- Use `best_model.pt` to load a pre-trained model for evaluation if you do not wish to train from scratch.
- `Trading_Eval.ipynb` is intended for more focused performance assessment and result visualization.

## Notes

- The model uses `yfinance` to download historical BTC-USD daily price data.
- The LSTM model includes engineered features such as returns, moving averages, ATR, and log returns.
- Backtrader is used to simulate algorithmic trading strategies and compare them with a buy-and-hold baseline.
- The notebook contains longer-running sections for random search, walk-forward analysis, and Monte Carlo simulation; these can be skipped for quicker experimentation.
- The repository includes a `.gitignore` configured to ignore generated CSV files, images, logs, model weights, and other runtime artifacts.

## Recommended Workflow

1. Install dependencies from `requirements.txt`.
2. Run `notebooks/BTC_LSTM.ipynb` to reproduce the main experiment.
3. Inspect the generated charts and metrics for evaluation.
4. Use the report `MSc_Project_Report_v1.pdf` to understand the methodology and results.

## License

This project is released under the MIT License. See `LICENSE` for details.
