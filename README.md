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
-Sample output from the function: `best("TX", "heart attack")`

#### Finding the Best Hospital in a State
- Write a function `best` that takes two arguments: the abbreviated name of a state and an outcome name.
- The function returns the name of the hospital with the lowest 30-day mortality for the specified outcome in that state.

#### Ranking Hospitals by Outcome in a State
- Write a function `rankhospital` that takes three arguments: the abbreviated name of a state (state), an outcome (outcome), and the ranking of a hospital in that state for that outcome (num).
- The function returns the name of the hospital with the specified ranking for the given outcome in that state. For example, the call
     ```r
  rankhospital("TX", "heart failure", 4)
  [1] "DETAR HOSPITAL NAVARRO"

  rankhospital("MN", "heart attack", 5000)
  [1] NA
- The ranking of the hospital- argument `num` in the function can take values `best`, `worst` or an `integer` indicating the ranking (small numbers are better)
- If the number given by num is larger than the number of hostpitals in that state, then the function should return **NA**.
- Hospitals that do not have data on a particular outcome should be excluded from the set of hospitals when deciding the rankings.
- **Handling ties:** If multiple hospitals have the same 30-day mortality rate for a given cause of death, those ties should be broken by using the hospital name whose letter of alphabet appear first.


#### Ranking Hospitals in All States
- Write a function `rankall` that takes two arguments: an outcome name (outcome) and a hospital ranking (num).
- The function returns a 2-column data frame containing the hospital in each state with the specified ranking for the given outcome.
- Make sure a value is returned for every state even if it has no entry specified in the hospital ranking (num). The value returned in such a case is `NA`. For example the call
    ```r
  head(rankall("heart attack", 20), 10)
returns
##                       hospital state
##                      <NA>    AK
## D W MCMILLAN MEMORIAL HOSPITAL AL
## ARKANSAS METHODIST MEDICAL CENTER AR
##                      <NA>    AZ
## JOHN C LINCOLN DEER VALLEY HOSPITAL AZ
## SHERMAN OAKS HOSPITAL              CA
## SKY RIDGE MEDICAL CENTER           CO
## MIDSTATE MEDICAL CENTER            CT
##                      <NA>    DC
##                      <NA>    DE


- The ranking of the hospital- argument `num` in the function can take values `best`, `worst` or an `integer` indicating the ranking (small numbers are better).
- Hospitals that do not have data on a particular outcome should be excluded from the set of hospitals when deciding the rankings.
- **Handling ties:** The `rankall` function should handle ties in the 30-day mortality rates in the same way that the `rankhospital` function handles ties.


