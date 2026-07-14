# IBM Applied Data Science Capstone

This repository contains the completed notebooks for the **Applied Data Science Capstone** project — the final course in IBM's Data Science Professional Certificate on Coursera. The project analyzes and predicts the landing success of the SpaceX Falcon 9 first stage, using data collection, wrangling, exploratory analysis, and machine learning.

## Overview

SpaceX advertises Falcon 9 launches at a fraction of the cost of competitors, largely because it reuses the first stage of the rocket. This project builds a predictive model to determine whether a Falcon 9 first stage will land successfully, which can help estimate launch costs for companies bidding against SpaceX.

## Repository Structure

| # | Notebook | Description |
|---|----------|-------------|
| 1 | `1. jupyter-labs-spacex-data-collection-api.ipynb` | Collects historical launch data via the SpaceX REST API and performs initial cleaning. |
| 2 | `2. jupyter-labs-webscraping.ipynb` | Scrapes Falcon 9 launch records from Wikipedia with BeautifulSoup and parses them into a DataFrame. |
| 3 | `3. labs-jupyter-spacex-Data-wrangling.ipynb` | Cleans and wrangles the combined dataset, engineering the landing outcome labels used for training. |
| 4 | `4. jupyter-labs-eda-sql-coursera_sqllite.ipynb` | Loads the data into a SQLite database and runs SQL queries to explore launch site, payload, and outcome trends. |
| 5 | `5. jupyter-labs-eda-dataviz.ipynb` | Exploratory data analysis and visualization with Matplotlib and Seaborn to uncover patterns in the data. |
| 6 | `6. lab_jupyter_launch_site_location.ipynb` | Interactive geographic visualization of launch sites and outcomes using Folium. |
| 7 | `7. SpaceX_Machine_Learning_Prediction_Part_5.ipynb` | Standardizes and splits the data, then trains and tunes classification models (Logistic Regression, SVM, Decision Tree, KNN) with GridSearchCV to predict landing success. |

The `alternate_versions/` folder contains JupyterLite/alternate variants of a few notebooks (data collection, data wrangling, ML prediction), kept for reference alongside the primary versions above.

## Results

Model performance was compared across several classifiers on the held-out test set, with the Decision Tree Classifier producing the best accuracy. Full metrics, confusion matrices, and model comparisons are in notebook 7.

## Tools & Libraries

- **Data collection & wrangling**: `requests`, `pandas`, `numpy`, BeautifulSoup
- **Database**: SQLite / `ipython-sql`
- **Visualization**: `matplotlib`, `seaborn`, `folium`
- **Machine learning**: `scikit-learn` (GridSearchCV, Logistic Regression, SVM, Decision Tree, KNN)

## Getting Started

```bash
git clone https://github.com/<your-username>/IBM-Applied-Data-Science-Capstone.git
cd IBM-Applied-Data-Science-Capstone
pip install -r requirements.txt
jupyter notebook
```

## Acknowledgments

- **IBM** for the course content and lab materials
- **Coursera** for hosting the IBM Data Science Professional Certificate
