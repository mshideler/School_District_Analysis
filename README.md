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

Before Removal
![District Summary 1](https://github.com/mshideler/School_District_Analysis/blob/main/Resources/District_Summary_Before_Removal.PNG)

After Removal
![District Summary 2](https://github.com/mshideler/School_District_Analysis/blob/main/Resources/District_Summary_After_Removal.PNG)

- Thomas High School Summary.  As can be seen in the pictures below, the % Passing Math, % Passing Reading and % Overall Passing all decreased significantly, around 25% - 30%, after the altered scores were removed; however, the Average Math and Reading Scores were barely affected.

Before Removal
![THS Summary 1](https://github.com/mshideler/School_District_Analysis/blob/main/Resources/THS_Summary_Before_Removal.png)

After Removal
![THS Summary 2](https://github.com/mshideler/School_District_Analysis/blob/main/Resources/THS_Summary_After_Removal.png)

After recalculating the above summaries, the Average Scores and % Passing Scores were recalculated for Thomas High School based on the math and reading scores for 10th – 12th graders.  The % Passing Scores were then replaced with the recalculated percentages.  Afterward, the following observations were made:

- Replacing the 9th graders math and reading scores had no effect on Thomas High School’s performance relative to other schools.  Thomas High School still ranked 2nd among the top five schools.

- The 9th grade math and reading scores for Thomas High School were both listed as “NaN” since that was what was used to replace the individual student scores.

- The spending range $630-$644 per student’s Average Scores and Passing Percentages all changed slightly.

Before the Recalculation
![Spending Before](https://github.com/mshideler/School_District_Analysis/blob/main/Resources/Spending_Before_Recalc.PNG)

After the Recalculation
![Spending After](https://github.com/mshideler/School_District_Analysis/blob/main/Resources/Spending_After_Recalc.PNG)

## Summary