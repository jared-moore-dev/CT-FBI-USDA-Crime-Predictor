# Data Overview

## Data Sources

This project integrates three primary data sources:

### 1. FBI Uniform Crime Reporting (UCR) Data
- **Source**: FBI Crime Data for Connecticut (2019)
- **File**: `connecticut_offense_type_by_agency_2019.xls`
- **Download**: Direct download from FBI UCR website
- **Key Metrics**: 
  - Comprehensive crime statistics by agency
  - Detailed breakdown of crime types
  - Includes offenses such as:
    - Crimes Against Persons
    - Crimes Against Property
    - Crimes Against Society
    - Specific crime categories (Assault, Homicide, etc.)

### 2. USDA Food Access Research Atlas Data
- **Source**: USDA Economic Research Service (2019)
- **File**: `FoodAccessResearchAtlasData2019.xlsx`
- **Download**: Direct download from USDA website
- **Key Metrics**:
  - Population demographics
  - Low-income and low-access tract information
  - Urban/rural classification
  - Poverty and income indicators
  - Food access metrics

### 3. Connecticut Census Tract to Town Mapping
- **Source**: CT Data Collaborative GitHub Repository
- **File**: `tract2town-2020.xlsx`
- **Download**: Direct download from GitHub
- **Purpose**: Geographical crosswalk between census tracts and town boundaries

## Data Processing Workflow

### Preprocessing Steps

1. **CT Town/FIPS Conversion**
   - Manually corrected missing town data for Willimantic and Groton
   - Ensured accurate tract-to-town mapping
   - Standardized tract FIPS codes

2. **Food Access Data Cleanup**
   - Filled blank values with zeros
   - Removed columns with all-zero values
   - Eliminated population share columns
   - Added town names based on tract FIPS codes
   - Aggregated data from tract level to town level

3. **Crime Data Processing**
   - Standardized column names
   - Removed agency type column

4. **Data Integration**
   - Merged Food Access and Crime data
   - Filtered to include only towns with crime data
   - Reordered columns to prioritize food access metrics

## Output Files

- `raw_output.xlsx`: Original raw data sheets
- `townrevised.xlsx`: Updated town and FIPS mapping
- `foodrevised.xlsx`: Cleaned food access data
- `foodaggregated.xlsx`: Town-level aggregated food access data
- `combined.xlsx`: Final merged dataset for machine learning

## Data Usage Notes

- Data represents Connecticut-specific information for the year 2019
- Aggregated at the town level for comprehensive analysis
- Carefully cleaned and cross-referenced across multiple sources

## Preprocessing Techniques

- Zero-filling for missing data
- Column pruning
- Geographical mapping
- Data aggregation
- Merge and filter operations

## Potential Limitations

- Data limited to Connecticut
- Some manual corrections were made
- 2019 data may not reflect current conditions

## Contact and Attribution

For questions about data sources or preprocessing:
- Consult original sources: FBI UCR, USDA ERS, CT Data Collaborative
- Reference GitHub repository for latest updates

## License
Respect original data source licensing terms for FBI, USDA, and CT Data Collaborative data