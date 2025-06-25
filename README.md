# Smart Lending Ally: AI-Powered Loan Recommendation System

## 🎯 Overview

Smart Lending Ally is an innovative AI-driven loan recommendation platform that revolutionizes how borrowers find the most suitable lending options in India's complex financial landscape. The system utilizes a unique dual-model classification approach combining XGBoost and Random Forest algorithms to predict loan eligibility across 10 prominent Indian banks with an impressive 98.33% average accuracy.

### Key Features

- **🤖 Dual-Model Classification**: Intelligently selects between XGBoost and Random Forest models based on performance metrics
- **🎯 Multi-Criteria Suitability Scoring**: Goes beyond simple eligibility to evaluate interest rates, processing times, and affordability
- **📊 Dynamic Weighting System**: Customized recommendations for 5 loan types (Home, Car, Education, Personal, Gold)
- **🏦 Multi-Bank Coverage**: Supports 10 major Indian banks including SBI, HDFC, ICICI, Axis Bank, and more
- **📈 Comprehensive Visualization**: User-friendly charts and explanations for transparent decision-making
- **🔍 Explainable AI**: Natural language explanations for all recommendations

## 🏗️ System Architecture

The Smart Lending Ally system follows a sophisticated pipeline:

1. **Data Preprocessing**: Feature engineering with financial ratios (DTI, LTI) and categorical encoding
2. **Dual-Model Training**: Comparative selection between Random Forest and XGBoost for each bank
3. **Suitability Scoring**: Multi-criteria evaluation using weighted factors
4. **Recommendation Generation**: Ranked suggestions with detailed explanations
5. **Visualization**: Interactive charts and comprehensive reports

## 📊 Dataset

The system uses a comprehensive dataset featuring:

- **2,000 synthetic loan application profiles** representing realistic Indian financial scenarios
- **25 features per profile** including demographics, financial details, and loan specifics
- **10 major Indian banks** with specific eligibility criteria
- **5 loan categories**: Home, Car, Education, Personal, and Gold loans
- **Income range**: ₹15,000 to ₹200,000 monthly
- **CIBIL scores**: 300 to 900 range

### Supported Banks

| Bank | Accuracy | Model Used |
|------|----------|------------|
| IndusInd Bank | 99.25% | XGBoost |
| ICICI Bank | 98.75% | XGBoost |
| Punjab National Bank | 98.50% | XGBoost |
| Kotak Mahindra Bank | 98.50% | XGBoost |
| HDFC Bank | 98.25% | XGBoost |
| Axis Bank | 98.25% | XGBoost |
| State Bank of India | 97.75% | XGBoost |
| Union Bank of India | 97.50% | XGBoost |
| Bank of Baroda | 97.50% | XGBoost |
| Canara Bank | 96.75% | XGBoost |


## 🚀 Getting Started

### Prerequisites

- Python 3.11 or higher
- 16 GB RAM (recommended)
- Intel Core i7 processor or equivalent

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/smart-lending-ally.git
cd smart-lending-ally
```

2. Install required dependencies:
```bash
pip install scikit-learn xgboost pandas numpy matplotlib seaborn plotly jupyter
```

3. Launch Jupyter Notebook:
```bash
jupyter notebook
```

4. Open the main notebook:
```bash
smart_lending_ally.ipynb
```

### Quick Start

1. **Open the Jupyter Notebook**: Launch `smart_lending_ally.ipynb` in your Jupyter environment

2. **Run all cells**: Execute the notebook cells sequentially to:
   - Load and preprocess the synthetic dataset
   - Train the dual-model classification system
   - Generate loan recommendations

3. **Customize input profiles**: Modify the applicant profile in the notebook:
```python
# Example profile (modify in the notebook)
profile = {
    'age': 42,
    'monthly_income': 150000,
    'cibil_score': 810,
    'loan_type': 'Home',
    'loan_amount': 8000000,
    'employment_years': 15
    # ... other features
}
```

4. **View results**: The notebook will generate:
   - Eligibility predictions for all 10 banks
   - Suitability scores and rankings
   - Interactive visualizations
   - Detailed recommendations with explanations

## 📈 Performance Metrics

### Model Performance
- **Average Accuracy**: 98.33% across all banks
- **Recommendation Precision**: 96.7% when validated against expert evaluations
- **Processing Time**: Real-time recommendations
- **Scalability**: Handles diverse user profiles effectively

### Key Improvements Over Existing Systems
- **20-28% higher accuracy** compared to single-algorithm systems (70-87%)
- **Comprehensive suitability scoring** beyond basic eligibility
- **Transparent explanations** for all recommendations
- **Dynamic weighting** based on loan type priorities

## 🔧 Technical Implementation

### Core Algorithms

**Suitability Score Calculation:**
```
S(P,B) = wE·E(P,B) + wI·I(P,B) + wP·P(P,B) + wA·A(P,B)
```

Where:
- E(P,B): Eligibility component (0-1)
- I(P,B): Interest rate favorability (0-1)  
- P(P,B): Processing efficiency (0-1)
- A(P,B): Affordability component (0-1)
- w: Loan-type specific weights

**Financial Ratios:**
- Debt-to-Income Ratio (DTI): `CurrentEMI / MonthlyIncome`
- Loan-to-Income Ratio (LTI): `LoanAmount / AnnualIncome`

### Dependencies

The main notebook requires the following Python libraries:

```
scikit-learn>=1.3.0
xgboost>=1.7.0
pandas>=2.0.0
numpy>=1.24.0
matplotlib>=3.7.0
seaborn>=0.12.0
plotly>=5.14.0
jupyter>=1.0.0
```

Install all dependencies with:
```bash
pip install scikit-learn xgboost pandas numpy matplotlib seaborn plotly jupyter
```

## 📊 Usage Examples

### Example 1: High-Income Professional
Open the notebook and locate the applicant profile section. Modify as needed:
```python
# In the notebook, find and modify the profile dictionary
profile = {
    'name': 'Arjun Sharma',
    'age': 42,
    'monthly_income': 150000,
    'cibil_score': 810,
    'loan_type': 'Home',
    'loan_amount': 8000000,
    'employment_years': 15,
    'existing_loans': 0
}
```

### Example 2: First-Time Car Buyer
```python
# Modify the profile in the notebook for car loan scenario
profile = {
    'age': 28,
    'monthly_income': 45000,
    'cibil_score': 720,
    'loan_type': 'Car',
    'loan_amount': 800000,
    'employment_years': 3
}
```

**Note**: All examples and modifications should be made directly in the Jupyter notebook.

## 🎨 Visualization Features

The system provides comprehensive visualizations:

- **Eligibility Radar Charts**: Multi-bank eligibility probability comparison
- **Suitability Score Bar Charts**: Detailed scoring breakdown
- **Interest Rate Comparisons**: Side-by-side rate analysis
- **Processing Time Charts**: Bank efficiency comparisons
- **Recommendation Explanations**: Natural language justifications

## 🔬 Research Contributions

This work contributes to the field through:

1. **Novel Dual-Model Classification**: Strategic combination of XGBoost and Random Forest
2. **Multi-Criteria Suitability Framework**: Holistic evaluation beyond basic eligibility
3. **Dynamic Weighting System**: Loan-type specific prioritization
4. **Explainable AI Integration**: Transparent recommendation reasoning
5. **Comprehensive Validation**: Real-world scenario testing across diverse user profiles

## 📚 Documentation

- [Research Paper](docs/Smart_Lending_Ally_Research_Paper.pdf) - Complete IEEE conference paper
- [Jupyter Notebook](smart_lending_ally.ipynb) - Full implementation with examples
- Sample Outputs - Available in `docs/sample_outputs/` folder

## 🤝 Contributing

We welcome contributions! To contribute:

1. Fork the repository
2. Create a new branch for your feature
3. Make changes to the Jupyter notebook
4. Test your modifications
5. Submit a pull request with detailed description

### Development Guidelines
- Follow PEP 8 style guidelines for Python code
- Add comments and markdown cells to explain complex sections
- Test with different applicant profiles
- Update documentation as needed

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Contact

**Research Team - Jain (Deemed-to-be University)**

- Rahul Rajasekharan Menon - 22btrcn222@jainuniversity.ac.in
- Tejas Rao M N - 22btrcn296@jainuniversity.ac.in
- Nikhil Reddy K - 22btrcn188@jainuniversity.ac.in
- Vishal Kumar P - 22btrcn194@jainuniversity.ac.in
- Nakul Govind S - 22btrcn180@jainuniversity.ac.in

**Faculty Supervisor**
- Dr. A. Balajee - balajee.a@jainuniversity.ac.in

## 🙏 Acknowledgments

- Jain (Deemed-to-be University) for research support
- Reserve Bank of India (RBI) for financial data insights
- National Centre for Financial Education (NCFE) for literacy statistics
- Indian banking sector for providing realistic lending criteria

## 📈 Future Work

- Integration with real-time banking APIs
- Regional loan product variations
- Additional specialized loan categories
- Mobile application development
- Advanced risk assessment models
