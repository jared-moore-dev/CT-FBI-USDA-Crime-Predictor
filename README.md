# CT_FBI_USDA_Predictor

# Food Security's Role in Predicting Physical Security

This repository contains the code, data, and findings from the project **"Hungry Hands: Food Security's Role in Predicting Physical Security"** by Jared M. Moore, submitted for **Case Studies in Machine Learning** at the University of Texas, Austin.

## Abstract
Food insecurity is a pressing public health challenge linked to increased crime rates and violence. This project explores the relationship between food access, socioeconomic factors, and crime in Connecticut. Using data from the USDA Food Access Research Atlas, FBI crime reports, and census tract demographics, we analyze the impact of food insecurity on physical security. Machine learning models were applied to assess predictive relationships, with key findings indicating:

- Poverty rates and SNAP enrollment as strong predictors of crime.
- Limited predictive power of food-insecure children data due to granularity.
- KNN regression outperforming neural networks for geospatial crime prediction.

## Repository Structure

```plaintext
├── data/
│   ├── combined.xlsx              # Preprocessed and combined dataset used in analysis
│   ├── Combined_Raw_Data.xlsx     # .xlsx data files (FBI, USDA, etc.) each in their own sheet
│   ├── README.md                  # Data descriptions and sources
├── notebooks/
│   ├── CSML_Project.ipynb         # Data Download, Processing, Combination, Training, and Results all-in-one file
├── results/
│   ├── ClusteringSVD.png          # SVD-based clustering visualization
│   ├── ClusteringT-SNE.png        # t-SNE clustering visualization
│   ├── CorrelationMatrix.png      # Correlation matrix visualization
│   ├── CTPredictionsvsActual.png  # Comparison of predicted vs actual values
│   ├── DistributionBoxPlot.png    # Box plot of data distribution
│   ├── DistributionGraph.png      # General data distribution graph
│   ├── DistributionJitter.png     # Jitter plot for data distribution
│   ├── ElbowMethodSVD.png         # SVD elbow method visualization
│   ├── ElbowMethodT-SNE.png       # t-SNE elbow method visualization
│   ├── Histogram.png              # Histogram visualization
│   ├── Income2Offenses.png        # Income-to-offenses relationship
│   ├── ModelEvaluationR-Square.png # R-squared evaluation of models
│   ├── PairplotMatrix.png         # Pair plot matrix visualization
│   ├── Population2Offenses.png    # Population-to-offenses relationship
│   ├── ScatterPlot.png            # General scatter plot
│   ├── SVD1.png                   # Visualization of first SVD component
│   ├── TSNEData.png               # Data visualization with t-SNE
├── README.md                      # Project overview
├── LICENSE                        # Licensing information
└── requirements.txt               # Dependencies
```

## Getting Started

### Prerequisites
Ensure you have Python 3.9+ installed. Required libraries can be installed via pip:

```bash
pip install -r requirements.txt
```

### Data Sources
1. **USDA Food Access Research Atlas** (2019): [Dataset link](https://www.ers.usda.gov/data-products/food-access-research-atlas/)
2. **FBI Crime Reports** (2019): [Dataset link](https://ucr.fbi.gov/crime-in-the.u.s/2019/crime-in-the-u.s.-2019/tables/table-8/table-8-state-cuts/connecticut.xls)
3. **CT Data Collaborative**: [Dataset link](https://www.ctdata.org/)

### Running the Analysis

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/food-crime-analysis.git
   cd food-crime-analysis
   ```

2. Preprocess the data:
   ```bash
   python src/utils.py preprocess
   ```

3. Run model training and evaluation:
   ```bash
   python src/models.py train
   ```

4. Explore the results in `results/` directory or use Jupyter notebooks for step-by-step analysis.

### Key Visualizations
- **Correlation Matrix**: Highlights relationships between socioeconomic factors, food security, and crime.
- **t-SNE Visualization**: Shows clustering of geospatial crime data.
- **Model Performance Comparison**: Demonstrates KNN regression's effectiveness in predicting crime.

## Key Findings
- **KNN Regression** emerged as the most accurate model for crime prediction.
- **Neural Networks** underperformed due to data sparsity and limited granularity.
- **Policy Implications**: Addressing food insecurity, alongside fostering social cohesion, can reduce crime rates in vulnerable communities.

## Future Work
- Extend analysis to other regions for generalizability.
- Incorporate additional sociological factors and public policy data.
- Explore optimized neural networks with larger amounts of data

## Contributing
Contributions are welcome! Please fork this repository, make changes, and submit a pull request.

## License
This project is licensed under the MIT License. See `LICENSE` for more details.

## Acknowledgments
- **University of Texas, Austin**
- **USDA Food Access Research Atlas**
- **FBI Uniform Crime Reporting Program**
- **CT Data Collaborative**

---
For questions or collaborations, please contact **Jared M. Moore** via [LinkedIn](https://linkedin.com/in/your-profile) or open an issue in this repository.
