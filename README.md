# School_District_Analysis

## Overview of the School District Analysis

The school board reviewed the school district analysis and believed the math and reading scores were altered for 9th graders at Thomas High Scholl.  The purpose of this analysis is to reevaluate the school district analysis after removing the altered scores.

Here is the code used to remove the altered math and reading scores:
```
student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"), ["reading_score"]] = np.nan

student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"), ["math_score"]] = np.nan
```

## Results

The removal of the altered scores affected the following:

- District Summary.  As can be seen in the pictures below, the Average Math Score, % Passing Math, % Passing Reading and % Overall Passing all decreased slightly.

