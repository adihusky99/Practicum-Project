# Practicum-Project
Practicum projects
## DA5020.P1 (2).Rmd

This is an R Markdown document that performs a comprehensive data analysis on substance abuse treatment admissions in New York State. Let me break down what each section does:
Document Setup
The document begins by loading essential R libraries for data manipulation (tidyverse, dplyr), string processing (stringr), and visualization (ggplot2).
Part 1: Basic R Operations
Questions 1-2: Creates a simple doctor dataset and demonstrates basic data frame indexing operations like accessing specific rows, columns, and ranges.
Question 3: Loads the built-in mtcars dataset and creates a scatter plot showing the relationship between car weight (wt) and fuel efficiency (mpg). The plot reveals a negative correlation - heavier cars get worse gas mileage.
Question 4: Calculates summary statistics and performs a Pearson correlation test, confirming a strong negative correlation (-0.87) between weight and MPG.
Part 2: Substance Abuse Data Analysis
Question 1: Imports real substance abuse treatment data from New York State's open data portal.
Question 2: Performs extensive data cleaning:

Removes rows with missing values
Standardizes column names with underscores
Creates frequency distributions to identify outliers
Analyzes admission numbers, finding that extremely high values come from populous NYC counties (Manhattan) for alcohol treatment, suggesting these are legitimate rather than data errors

Question 3: Creates coded versions of categorical variables to make the dataset more compact:

Counties get 2-letter codes (e.g., "NY" for New York County)
Program categories get 3-letter abbreviations
Age groups get simplified ranges (e.g., "18-24")
Substance types get 3-letter codes

Question 4: Develops a function annualAdmissions() that creates a time series visualization showing total admissions from 2007-2021. The chart reveals:

Generally declining admissions over time
A peak in 2009 (311,717 admissions)
Sharp drops in 2020-2021, likely due to COVID-19 impacts

Question 5: Analyzes geographic distribution of admissions, finding that the top 5 counties (all NYC boroughs plus Suffolk) account for 45.7% of all state admissions, reflecting population density patterns.
Question 6: Focuses specifically on rehabilitation facilities using pattern matching:

Uses grepl() with regular expressions to filter for various types of rehab services
Identifies the most common substance by age group:

Under 18: Marijuana
18-34: Heroin
35+: Alcohol


Creates a bar chart visualizing these age-specific substance abuse patterns

Key Insights
The analysis reveals important public health patterns: younger people primarily struggle with marijuana and heroin, while older adults primarily have alcohol dependencies. Geographic concentration in urban areas highlights where resources are most needed. The COVID-19 impact on treatment access is also clearly visible in the data.
This type of analysis is crucial for public health officials to understand substance abuse trends and allocate treatment resources effectively.
