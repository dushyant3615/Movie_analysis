## Movie Analysis (IMDb Top 1000)

This project explores the IMDb Top 1000 dataset and trains a regression model (Random Forest) to predict IMDb ratings. The notebook includes robust preprocessing via an sklearn Pipeline and generates plots saved to disk.

### Requirements
- Python 3.9+
- Packages: pandas, numpy, scikit-learn, matplotlib, seaborn

You can install them from inside the notebook or locally:

```bash
pip install -r requirements.txt
# or, from the first notebook cell: %pip install -q pandas numpy scikit-learn matplotlib seaborn
```

### Files
- `imdb.ipynb`: Main analysis and modeling notebook
- `imdb_top_1000.csv`: Dataset (place in the project root)
- `feature_importance.png`: Top features by importance (created after running notebook)
- `predicted_vs_actual.png`: Scatter plot of predictions vs actual ratings (created after running notebook)

### How to Run
1. Ensure `imdb_top_1000.csv` is in the project root (same folder as the notebook).
2. Open `imdb.ipynb` in Jupyter/Colab/VScode.
3. Run all cells. The pipeline will:
   - Load and preprocess data
   - Train a RandomForestRegressor with parallelism
   - Evaluate metrics: MSE, MAE, R2
   - Save plots to the project folder

### Outputs
- `feature_importance.png`: Bar chart of top 15 features used by the model.
- `predicted_vs_actual.png`: Predicted vs actual IMDb ratings with reference line.

### Notes
- The notebook automatically detects the dataset path for both local and Colab runs.
- Preprocessing is handled by an sklearn `Pipeline` and `ColumnTransformer`, ensuring reproducibility.


