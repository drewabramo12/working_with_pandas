# working_with_pandas

## Overview of school district analysis

The purpose of this analysis was to depict the relationship between student success through factors of math, reading and overall passing percentage against factors of school size and budget per student. This analysis found that the specific subgroup of Thomas High School students in the 9th grade had faulty data. The deeper challenge from this analysis was enacting the cleaning of Thomas High School 9th grade students and the subsequent reapplying to the school_data_complete_df for analysis.

## Results

- How is the district summary affected?

The district summary is unchanged.

Original:
![Original District summary](https://github.com/drewabramo12/working_with_pandas/blob/main/Resources/district_summary_original.PNG)

New:
![New District summary](https://github.com/drewabramo12/working_with_pandas/blob/main/Resources/district_summary_new.PNG)

- How is the school summary affected?

School summary's math, reading, and overall passing percentages for Thomas High School increase substantially by a relative 30%.

Orginal:
![Original School summary](https://github.com/drewabramo12/working_with_pandas/blob/main/Resources/per_school_sum_original.PNG)

New:
![New School summary](https://github.com/drewabramo12/working_with_pandas/blob/main/Resources/per_school_sum_new.PNG)


- How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

Thomas High School's average math and reading scores are unaffected by the change.

- How does replacing the ninth-grade scores affect the following:
    - Math and reading scores by grade

Original Math:
![Original Grade Math Passing](https://github.com/drewabramo12/working_with_pandas/blob/main/Resources/grade_math_passing_original.PNG)

New Math:
![New Grade Math Passing](https://github.com/drewabramo12/working_with_pandas/blob/main/Resources/grade_math_passing_new.PNG)

Original Reading:
![Original Grade Reading Passing](https://github.com/drewabramo12/working_with_pandas/blob/main/Resources/grade_reading_passing_original.PNG)

New Reading:
![New Grade Reading Passing](https://github.com/drewabramo12/working_with_pandas/blob/main/Resources/grade_reading_passing_new.PNG)
    The math score for Thomas high school's 9th grade class went from 83.6% to nan. The reading score for Thomas high school's 9th grade class went from 83.7% to nan.

    - Scores by school spending

    The scores by school spending had no differences, however; I did initially find that the original school spending data frame had 100% for all passing reading percentages. This led me to find an initial error in the original code. I was able to trouble shoot by following the variables backwards and discovered that there was a copying error with the line of code `per_school_passing_reading = school_data_complete_df.groupby(['school_name']).count()['student_name']`. This code in actuality should have been `per_school_passing_reading = per_school_passing_reading.groupby(['school_name']).count()['student_name']` and was adjusted as such.

Original School Spending:
![Original School Spending](https://github.com/drewabramo12/working_with_pandas/blob/main/Resources/school_spending_original.PNG)

New School Spending:
![New School Spending](https://github.com/drewabramo12/working_with_pandas/blob/main/Resources/school_spending_new.PNG)

    - Scores by school size

    The scores by school size did not change.

Original School Spending:
![Original School Size](https://github.com/drewabramo12/working_with_pandas/blob/main/Resources/school_size_original.PNG)

Original School Spending:
![New School Size](https://github.com/drewabramo12/working_with_pandas/blob/main/Resources/school_size_new.PNG)

    - Scores by school type

    The scores by school type did not change.

Original School Spending:
![Original School Type](https://github.com/drewabramo12/working_with_pandas/blob/main/Resources/CD_original.PNG)

Original School Spending:
![Original School Type](https://github.com/drewabramo12/working_with_pandas/blob/main/Resources/CD_original.PNG)