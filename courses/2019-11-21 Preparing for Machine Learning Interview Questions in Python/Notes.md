
# Simple Imputer

```
# Import imputer module
from sklearn.impute import SimpleImputer

# Subset numeric features: numeric_cols
numeric_cols = loan_data.select_dtypes(include=[np.number])

# Impute with mean
imp_mean = SimpleImputer(strategy='mean')
loans_imp_mean = imp_mean.fit_transform(numeric_cols)

# Convert returned array to DataFrame
loans_imp_meanDF = pd.DataFrame(loans_imp_mean, columns=numeric_cols.columns)
```
【Output】   
```
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 88910 entries, 0 to 88909
Data columns (total 13 columns):
Current Loan Amount             88910 non-null float64
Credit Score                    88910 non-null float64
Years in current job            88910 non-null float64
Annual Income                   88910 non-null float64
Monthly Debt                    88910 non-null float64
Years of Credit History         88910 non-null float64
Months since last delinquent    88910 non-null float64
Number of Open Accounts         88910 non-null float64
Number of Credit Problems       88910 non-null float64
Current Credit Balance          88910 non-null float64
Maximum Open Credit             88910 non-null float64
Bankruptcies                    88910 non-null float64
Tax Liens                       88910 non-null float64
dtypes: float64(13)
memory usage: 8.8 MB
None
```

# Iterative imputation

