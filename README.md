# San Francisco Bicycle Racks Installation Analysis

This project explores the bicycle rack installations across San Francisco, examining installation patterns, geographical distribution, and temporal trends. 
The analysis aims to: <br>
- Understand the spatial distribution of bicycle racks <br>
- Analyze installation trends over time <br>
- Identify patterns in rack placement and neighborhood distribution <br>
- Forecast future installation needs. </p>
It combines the use of R and Rmarkdown, resulting in a user-friendly interface available in an html file format.

Hypotheses: <br>
1. The number of bicycle parking racks installed has increased over time. <br>
2. Neighborhoods with higher population density or commercial activity have more racks installed. <br>
3. Bicycle racks are more frequently installed during certain months, aligning with cycling-friendly weather.</br>

Datatest:
<p>The data is sourced from San Francisco Open Data Portal. The dataset contains information about public bicycle parking installations, including location details, installation dates, and capacity information. 

Below is an overview of the step-by-step analysis.

1. INITIAL SETUP AND DATA PREPARATION
a) Environment Setup:
   - Set Project as working directory
   - Installed and loaded required packages (tidyverse, lubridate, corrplot, forecast, kableExtra, RSQLite, leaflet, DT)
   - Configured RMarkdown settings (echo=TRUE, warning=FALSE, message=FALSE)

b) Data Loading:
   - Imported 'Bicycle_Parking_Racks_20241211.csv'
   - Initial data inspection (structure, missing values, data types)
   - Basic data cleaning and validation

2. DATA PREPROCESSING
a) Data Cleaning:
   - Converted PLACEMENT to factor
   - Handled missing values in INSTALL_MO
   - Extracted coordinates from shape column
   - Removed records with missing INSTALL_YR

b) Feature Engineering:
   - Created INSTALL_DATE from INSTALL_YR and INSTALL_MO
   - Formatted date columns appropriately
   - Selected and organized relevant columns

3. SPATIAL ANALYSIS
a) Interactive Map Creation:
   - Initialized leaflet map
   - Added base tiles
   - Plotted bicycle rack locations with popup information such as address, racks, spaces, installation year

4. DESCRIPTIVE STATISTICS
a) Basic Statistics:
   - Calculated total number of racks and spaces
   - Summarized by location
   - Analyzed placement types

b) Distribution Analysis:
   - Analyzed rack distribution by neighborhood
   - Studied placement type patterns
   - Examined installation trends

5. TEMPORAL ANALYSIS
a) Time-based Patterns:
   - Analyzed yearly installation trends
   - Studied monthly patterns
   - Identified seasonal variations

b) Growth Analysis:
   - Calculated cumulative installations
   - Analyzed year-over-year growth
   - Identified peak installation periods

6. CORRELATION ANALYSIS
a) Variable Relationships:
   - Created correlation matrix
   - Generated correlation plot
   - Analyzed relationships between variables

7. PREDICTIVE MODELING
a) Time Series Analysis:
   - Prepared time series data
   - Fitted ARIMA model
   - Generated 5-year forecast


8. CONCLUSIONS AND RECOMMENDATIONS
a) Key Findings:
   - Summarized spatial distribution
   - Highlighted temporal trends
   - Identified key patterns

b) Recommendations: shared a few recommendations based on data insights.
   - Address underserved areas
   - Optimize installation scheduling
   - Plan maintenance strategy

9. DATABASE CREATION
SQLite Setup:
   - Created database structure
   - Defined tables (bike_racks, locations)
   - Imported processed data.
