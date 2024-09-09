# The Relationship Between Economic and Health Status

## Overview

This project explores the relationship between economic status and self-reported health status in the United States. Utilizing data from the Kaiser Family Foundation's State Health Facts page, the study examines how variations in economic conditions impact health outcomes across different states, races, and regions.

## Dataset Overview

### FederalPovertyLevel.csv

Contains data on the distribution of the population by federal poverty level in each state and the overall country.

- **Location**: Geographic area (e.g., United States, Alabama, Alaska)
- **Under 100%**: Proportion of the population living under 100% of the federal poverty level
- **100-199%**: Proportion of the population living between 100% and 199% of the federal poverty level
- **200-399%**: Proportion of the population living between 200% and 399% of the federal poverty level
- **400%+**: Proportion of the population living above 400% of the federal poverty level
- **Total**: Always sums to 1 (representing 100% of the population distributed across categories)

### HealthStatus.csv

Breaks down the proportion of adults reporting fair or poor health status by race/ethnicity and overall.

- **Location**: Geographic area (e.g., United States, Alabama, Alaska)
- **All Adults**: Proportion of all adults reporting fair or poor health status
- **White**: Proportion of White adults reporting fair or poor health status
- **Black**: Proportion of Black adults reporting fair or poor health status
- **Hispanic**: Proportion of Hispanic adults reporting fair or poor health status
- **Asian/ Native Hawaiian or Pacific Islander**: Proportion of Asian, Native Hawaiian, or Pacific Islander adults reporting fair or poor health status
- **American Indian/ Alaska Native**: Proportion of American Indian or Alaska Native adults reporting fair or poor health status
- **Other**: Proportion of adults from other races/ethnicities reporting fair or poor health status

## Methodology

1. **Data Import and Cleaning**:
   - Imported both CSV files using pandas.
   - Filtered out data for U.S. territories.
   - Selected relevant columns for analysis.

2. **Data Merging**:
   - Merged FederalPovertyLevel and HealthStatus datasets on location.

3. **Correlation Analysis**:
   - Calculated correlation coefficients between:
     - The percentage of the population living under 100% of the federal poverty level and the proportion of adults reporting fair or poor health status.
     - The percentage of the population living above 400% of the federal poverty level and the proportion of adults reporting fair or poor health status.
     - The percentage of the population living between 200% and 399% of the federal poverty level and the proportion of adults reporting fair or poor health status.

4. **Visualization**:
   - **Figures**:
     - **Figure 1**: Scatter plot of health status vs. the percentage of the population under 100% of the federal poverty level.
     - **Figure 2**: Scatter plot of health status vs. the percentage of the population over 400% of the federal poverty level.
     - **Figure 3**: Scatter plot of health status vs. the percentage of the population between 200-399% of the federal poverty level.
     - **Figure 4**: Bar chart showing the percentage of adults reporting fair or poor health by region and race.

5. **Regional Analysis**:
   - Grouped states into regions and calculated average health status by region.
   - Visualized health status disparities by region and race using bar charts.

## Results

- **Correlation Coefficients**:
  - **Under 100% Poverty**: r = 0.812 (strong positive correlation with poor health status).
  - **Over 400% Poverty**: r = -0.790 (strong negative correlation with poor health status).
  - **200-399% Poverty**: r = 0.402 (weaker correlation, indicating variability).

- **Regional Insights**:
  - The South and Southwest regions have higher percentages of poor health compared to the Northeast.
  - Health disparities are evident among different racial groups, with Native Americans, Black, and Hispanic individuals reporting poorer health compared to White and Asian individuals.

## Visualizations

1. **Health Status vs. Federal Poverty Level**:
   - Scatter plots illustrating the relationships between health status and federal poverty level categories.
   - Saved as SVG files: `under100.svg`, `over400.svg`, and `between200.svg`.

2. **Percent of Adults Reporting Fair or Poor Health by Region**:
   - Bar chart displaying average health status across U.S. regions and racial groups.
   - Saved as an SVG file: `barchart.svg`.

## Future Research

- **Investigate** the ambiguous relationship for middle-income earners and identify additional influencing factors such as diet, physical activity, and smoking.
- **Analyze** how regional and racial factors interact with economic status to affect health outcomes.
- **Develop** targeted public health interventions and policies based on the findings to address health disparities and improve equity.

## Works Cited

- KFF’s State Health Facts. Data Source: 2008-2022 American Community Survey, 1-Year Estimates.
- KFF’s State Health Facts. Data Source: The Centers for Disease Control and Prevention (CDC)'s 2013-2022 Behavioral Risk Factor Surveillance System (BRFSS).

