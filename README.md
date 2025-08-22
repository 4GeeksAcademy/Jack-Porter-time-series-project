# Time Series Forecasting with Python

[![Codespaces Prebuilds](https://github.com/4GeeksAcademy/gperdrizet-time-series-project/actions/workflows/codespaces/create_codespaces_prebuilds/badge.svg)](https://github.com/4GeeksAcademy/gperdrizet-time-series-project/actions/workflows/codespaces/create_codespaces_prebuilds)

A comprehensive data science project focused on time series analysis and forecasting using Python. This project demonstrates essential time series modeling techniques, from exploratory data analysis to advanced ARIMA modeling with proper validation methodologies.

## Project Overview

This project analyzes time series data using the Airline Passengers dataset (from Seaborn). The dataset contains airline passenger counts from 1949 to 1960, showcasing clear seasonal patterns and an upward trend. The goal is to implement various forecasting models, including baseline approaches and advanced ARIMA modeling, while ensuring proper validation techniques are applied.

The project provides hands-on experience with:

- Time series data preprocessing and datetime handling
- Exploratory data analysis for temporal data
- Baseline model implementation (linear regression, carry-forward)
- Stationarity testing and data transformation
- ARIMA model training with automatic parameter selection
- Proper time series validation using TimeSeriesSplit
- Model evaluation and performance comparison

## Getting Started

### Option 1: GitHub Codespaces (Recommended)

1. **Fork the Repository**
   - Click the "Fork" button on the top right of the GitHub repository page
   - 4Geeks students: set 4GeeksAcademy as the owner - 4Geeks pays for your codespace usage. All others, set yourself as the owner
   - Give the fork a descriptive name. 4Geeks students: I recommend including your GitHub username to help in finding the fork if you lose the link
   - Click "Create fork"
   - 4Geeks students: bookmark or otherwise save the link to your fork

2. **Create a GitHub Codespace**
   - On your forked repository, click the "Code" button
   - Select "Create codespace on main"
   - If the "Create codespace on main" option is grayed out - go to your codespaces list from the three-bar menu at the upper left and delete an old codespace
   - Wait for the environment to load (dependencies are pre-installed)

3. **Start Working**
   - Open `notebooks/mvp.ipynb` in the Jupyter interface
   - Follow the step-by-step instructions in the notebook
   - Reference `notebooks/solution.ipynb` for complete implementations

### Option 2: Local Development

1. **Prerequisites**
   - Git
   - Python >= 3.10

2. **Fork the repository**
   - Click the "Fork" button on the top right of the GitHub repository page
   - Optional: give the fork a new name and/or description
   - Click "Create fork"

3. **Clone the repository**
   - From your fork of the repository, click the green "Code" button at the upper right
   - From the "Local" tab, select HTTPS and copy the link
   - Run the following commands on your machine, replacing `<LINK>` and `<REPO_NAME>`

   ```bash
   git clone <LINK>
   cd <REPO_NAME>
   ```

4. **Set Up Environment**

   ```bash
   python -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

5. **Launch Jupyter & start the notebook**
   ```bash
   jupyter notebook notebooks/mvp.ipynb
   ```

## Project Structure

```
├── .devcontainer/      # Development container configuration
├── data/               # Data directories
├── models/             # Trained models directory
│
├── notebooks/          # Jupyter notebook directory
│   ├── mvp.ipynb       # Assignment notebook with exercises
│   └── solution.ipynb  # Complete solution notebook
│
├── .gitignore          # Files/directories not tracked by git
├── LICENSE             # Project license
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation
```

## Dataset: Airline Passengers
- **Source**: Seaborn built-in dataset
- **Features**: Monthly passenger numbers from 1949-1960
- **Characteristics**: Clear seasonal patterns and upward trend
- **Use case**: Classic time series forecasting example



## Learning Objectives

1. **Data Preprocessing**: Convert string dates to datetime objects and set proper time series indices
2. **Baseline Models**: Implement simple linear regression and carry-forward prediction models
3. **Exploratory Data Analysis**: 
   - Visualize time series data
   - Check for missing timepoints and regularity
   - Analyze distributions and extreme values
4. **Stationarity Analysis**: Use Augmented Dickey-Fuller test to assess stationarity
5. **ARIMA Modeling**: 
   - Automatic parameter selection with `auto_arima`
   - Seasonal ARIMA implementation
   - Understanding model limitations
6. **Proper Validation**: 
   - Time series train-test splitting
   - Cross-validation with `TimeSeriesSplit`
   - Model performance evaluation and comparison
7. **Critical Analysis**: Understanding when forecasting models fail and their limitations

## Key Insights from the Project

- **Baseline Importance**: Simple models often provide valuable performance benchmarks
- **Validation Complexity**: Time series data requires special consideration for train-test splitting
- **Model Limitations**: ARIMA models can exhibit repetitive patterns in long-term forecasts
- **Proper Evaluation**: Cross-validation reveals true model performance on unseen data

## Technologies Used

- **Python 3.11**: Core programming language
- **Pandas**: Time series data manipulation and analysis
- **NumPy**: Numerical computing and array operations
- **Matplotlib & Seaborn**: Data visualization and plotting
- **Scikit-learn**: Machine learning tools including TimeSeriesSplit
- **pmdarima**: Automated ARIMA modeling with `auto_arima`
- **SciPy**: Statistical analysis and testing
- **Statsmodels**: Statistical modeling including stationarity tests
- **Jupyter**: Interactive development environment

## Model Performance

The project implements and compares multiple forecasting approaches:

- **Linear Regression**: Simple trend-based forecasting
- **Carry Forward**: Using previous values as predictions
- **ARIMA**: Advanced time series modeling with automatic parameter selection

Performance is evaluated using Root Mean Square Error (RMSE) across different validation methodologies, demonstrating the importance of proper time series validation techniques.

## Contributing

This is an educational project. Contributions for improving the analysis, adding new datasets, or enhancing the modeling approaches are welcome:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is licensed under the terms specified in the LICENSE file.
