# Book Dataset Analysis

## Overview
This project explores a dataset containing information about books, focusing on data processing, transformation, and model evaluation. The project aims to derive insights, preprocess data for analysis, and apply machine learning models to predict book prices.

#### Transformations
- **Encoding**:
  - Ratings and Reviews columns were transformed into numerical formats for analysis.
  - One-hot encoding was applied to categorical features such as `BookCategory`.
  - Word embeddings were implemented for text-based columns like `Synopsis`, `Title`, and `Author`.
- **Feature Engineering**:
  - Extracted publication year and book format from the `Edition` column.
  - Removed redundant columns (e.g., `Genre` replaced by `BookCategory`).
- **Data Expansion**: Array columns were expanded to create a comprehensive dataset, resulting in 2,200 columns from the original 36.

---

### Model Implementation
Two machine learning models were tested to predict book prices:

#### Linear Regression
- **Performance Metrics**:
  - Mean Absolute Error (MAE): Exceptionally high.
  - Mean Squared Error (MSE): Extremely large.
  - R-squared: Negative, indicating poor model performance.
- **Insights**: The model struggled to capture underlying patterns, highlighting potential overfitting or data issues.

#### Random Forest Regressor
- **Performance Metrics**:
  - MAE: ~293.51.
  - MSE: ~291,089.59.
  - R-squared: ~0.1884.
- **Insights**: Demonstrated better predictive ability than Linear Regression but still showed room for improvement.
