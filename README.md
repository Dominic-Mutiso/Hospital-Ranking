## Programming Assignment 3: R Programming

### Introduction
This assignment involves working with data from the Hospital Compare website run by the U.S. Department of Health and Human Services. The dataset contains information about the quality of care at over 4,000 Medicare-certified hospitals in the U.S., focusing on 30-day mortality and readmission rates for heart attacks, heart failure, and pneumonia.

### Data
The dataset is provided in the file `ProgAssignment3-data.zip`, which contains:
- `outcome-of-care-measures.csv`: Information about 30-day mortality and readmission rates for heart attacks, heart failure, and pneumonia.
- `hospital-data.csv`: Information about each hospital.
- `Hospital_Revised_Flatfiles.pdf`: Descriptions of the variables in each file.

### Instructions

#### Plot the 30-day Mortality Rates for Heart Attack
- Read the data from `outcome-of-care-measures.csv`.
- Plot a histogram of the 30-day death rates from heart attacks.

#### Finding the Best Hospital in a State
- Write a function `best` that takes two arguments: the abbreviated name of a state and an outcome name.
- The function returns the name of the hospital with the lowest 30-day mortality for the specified outcome in that state.

#### Ranking Hospitals by Outcome in a State
- Write a function `rankhospital` that takes three arguments: the abbreviated name of a state, an outcome, and the ranking of a hospital in that state for that outcome.
- The ranking of the hospital- argument `num` in the functiontakes values `best`, `worst` or an `integer`  indicating the ranking (small numbers are better)
- The function returns the name of the hospital with the specified ranking for the given outcome in that state.

#### Ranking Hospitals in All States
- Write a function `rankall` that takes two arguments: an outcome name and a hospital ranking.
- The function returns a 2-column data frame containing the hospital in each state with the specified ranking for the given outcome.


