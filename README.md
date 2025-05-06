# 🩺 Diabetes Prediction & Analysis Dashboard

An interactive data exploration tool for the Pima Indians Diabetes Dataset, offering comprehensive visualization and statistical analysis to 
uncover significant patterns associated with diabetes diagnosis.



## 🔍 Overview


This project combines exploratory data analysis (EDA) with an interactive Streamlit dashboard to investigate the relationships between various health metrics and diabetes diagnoses in the Pima Indians population. The analysis focuses on identifying key risk factors and visualizing their distributions to gain deeper insights into diabetes prevalence patterns.


## 📊 Dataset Information


The Pima Indians Diabetes Dataset originates from the National Institute of Diabetes and Digestive and Kidney Diseases. It includes diagnostic measurements from 768 females of Pima Indian heritage, with the following features:


- **Pregnancies**: Number of times pregnant
- **Glucose**: Plasma glucose concentration (2 hours after an oral glucose tolerance test)
- **BloodPressure**: Diastolic blood pressure (mm Hg)
- **SkinThickness**: Triceps skin fold thickness (mm)
- **Insulin**: 2-Hour serum insulin (mu U/ml)
- **BMI**: Body mass index (weight in kg/(height in m)²)
- **DiabetesPedigreeFunction**: Diabetes pedigree function (genetic influence score)
- **Age**: Age in years
- **Outcome**: Class variable (0 = non-diabetic, 1 = diabetic)


**Source**: [Kaggle - Pima Indians Diabetes Database](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)


## ✨ Features


### Data Cleaning & Preparation
- **Zero-Value Handling**: Automatically identifies and replaces physiologically impossible zero values with feature-wise medians
- **Statistical Summaries**: Provides comprehensive descriptive statistics for all features
- **Missing Value Detection**: Identifies and reports any missing or problematic data points


### Interactive Visualizations
- **Distribution Analysis**: Boxplots with custom colors highlight the distribution of each health metric
- **Correlation Heatmaps**: Two types of heatmaps reveal relationships between variables:
- Standard correlation matrix for all features
- Enhanced custom heatmap with configurable parameters
- **Outcome Distribution**: Visual representation of the diabetic vs. non-diabetic population split


### User Interface
- **Tabbed Navigation**: Clean, organized interface with dedicated sections for data and visualizations
- **Interactive Controls**: Select specific features for visualization and analysis
- **Custom Styling**: Enhanced visual design for improved user experience


## 🚀 Installation


### Prerequisites
- Python 3.7+
- Git


### Setup Steps


#### 1. Clone the repository
```bash
git clone https://github.com/A-Mohammed19/Diabeties_Analysis.git
cd Diabeties_Analysis
```


#### 2. Set up virtual environment (recommended)
```bash
python -m venv venv


# On Windows
venv\Scripts\activate


# On macOS/Linux
source venv/bin/activate
```


#### 3. Install dependencies
```bash
pip install -r requirements.txt
```


## 💻 Usage


### Launch the Streamlit Dashboard
```bash
streamlit run streamlit_app.py
```


Your browser should automatically open to `http://localhost:8501` with the interactive dashboard ready to use.


### Dashboard Navigation


1. **Data Overview Tab**:
   - View dataset sample and basic information
   - Explore summary statistics, missing values, and zero counts


2. **Visualizations Tab**:
   - Select from different visualization types:
     - Class Distribution: See the balance of diabetic vs. non-diabetic cases
     - Feature Boxplots: Examine the distribution of each health metric
     - Correlation Heatmap: View relationships between all variables
     - Custom Heatmap: Create a focused correlation analysis on selected features


## 📁 Project Structure


```
diabetes-analysis/
│
├── data/                   # Dataset directory
│   └── diabetes.csv        # Raw dataset file
│
├── src/                    # Source code
│   ├── __init__.py         # Package initialization
│   ├── loading.py          # Data loading and preprocessing functions
│   ├── analysis.py         # Statistical analysis functions
│   └── visualizations.py   # Visualization functions
│
├── notebooks/              # Jupyter notebooks for EDA
│   └── exploratory_analysis.ipynb  # Initial data exploration
│
├── streamlit_app.py        # Main Streamlit application
├── requirements.txt        # Project dependencies
└── README.md               # Project documentation
```


## 🧹 Data Processing


The dashboard automatically handles data quality issues present in the original dataset:


- **Zero Value Replacement**: Physiologically impossible zero values in Glucose, BloodPressure, SkinThickness, Insulin, and BMI are identified and replaced with their respective median values
- **Statistical Analysis**: Comprehensive summary statistics are calculated for all features to provide context for the visualizations


## 📈 Visualizations


### Feature Distribution Boxplots
Customized boxplots display the distribution of each health metric with appropriate color coding:
- Pregnancies: Pink
- Glucose: Red
- BloodPressure: Light Green
- SkinThickness: Brown
- Insulin: Light Blue
- BMI: Purple
- DiabetesPedigreeFunction: Orange
- Age: Teal


### Correlation Analysis
Two different heatmap options provide insights into feature relationships:
- Standard correlation matrix shows all pairwise feature correlations
- Enhanced custom heatmap allows selection of specific features with configurable color palettes


## 🤝 Contributing


Contributions are welcome! Please feel free to submit a Pull Request.


1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request


---
## License

[MIT](LICENSE)

## Author

- A. Mohammed

