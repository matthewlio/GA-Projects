# Project 1: SAT & ACT Analysis

## Problem Statement

SAT and ACT are popular standardized tests for college admission in the US. Their purpose is to measure a high school student's readiness for college, and with one standardized score, colleges are able to compare all applicants. Overall, the higher the score on these tests, the more college options will become available.

In this analysis, we explore SAT and ACT score requirements to see the relationship between college prestige and test scores. Scores of applicants for each college major will be considered, and the correlation of all variables, including number of applicants and acceptance rates, will be thoroughly analysed. With derived insights, we want to make recommendations for ideal scores for test takers to aim for, giving them the chance of enrolment into their ideal college and major.

## Data Dictionary

### Dataset 1: Schools' admittance scores and acceptance rates
#### Dataset: df_college

|Feature|Type|Dataset|Description|
|---|---|---|---|
|school|object|ACT/SAT|The schools that admission test takers can apply for| 
|no_of_applicants|int|ACT/SAT|Number of applicants for the school| 
|accept_rate|float|ACT/SAT|School acceptance rate in terms of percentage| 
|sat_25th_perc|float|SAT|25th percentile score of all accepted applicants of the school that took SAT| 
|sat_75th_perc|float|SAT|75th percentile score of all accepted applicants of the school that took SAT| 
|sat_median|float|SAT|Median (50th percentile) score of all accepted applicants of the school that took SAT| 
|sat_median_pct|float|SAT|Median (50th percentile) score of all accepted applicants of the school that took SAT, converted to percentage| 
|act_25th_perc|float|ACT|25th percentile score of all accepted applicants of the school that took ACT| 
|act_75th_perc|float|ACT|75th percentile score of all accepted applicants of the school that took ACT| 
|act_median|float|ACT|Median (50th percentile) score of all accepted applicants of the school that took ACT| 
|act_median_pct|float|ACT|Median (50th percentile) score of all accepted applicants of the school that took ACT, converted to percentage| 
|applicants_accepted|int|ACT/SAT|Number of applicants accepted for the school| 

Assumptions were made that the median scores of both SAT and ACT lies directly between their 25th and 75th percentiles.

### Dataset 2: SAT Scores by Intended College Major
#### Dataset: df_major

|Feature|Type|Dataset|Description|
|---|---|---|---|
|int_college_major|object|SAT|College majors that admission test takers can apply for| 
|test_takers|int|SAT|Number of applicants for the college major| 
|test_takers_pct|float|SAT|Percentage of applicants that applied for the college major| 
|total_score|int|SAT|Average total score (Reading & Writing + Math) of applicants of the college major| 
|read_write|int|SAT|Average score for "Reading & Writing" section of applicants of the college major| 
|math|int|SAT|Average score for "Math" section of applicants of the college major| 
|total_score_pct|float|SAT|Average total score (Reading & Writing + Math) of applicants of the college major, converted to percentage| 
|read_write_pct|float|SAT|Average score for "Reading & Writing" section of applicants of the college major, converted to percentage| 
|math_pct|float|SAT|Average score for "Math" section of applicants of the college major, converted to percentage| 

## Conclusions and Recommendations

### Conclusions

### From dataset 1: Schools' admittance scores and acceptance rates

From the summary of statistics, we observed a summary of scores we could aim for:
- SAT 1070, ACT 22: Low chance for 25% of schools
- SAT 1175, ACT 25: Medium chance for 25% of schools
- SAT 1270, ACT 28: High chance for 25% of schools
- SAT 1150, ACT 24: Low chance for 50% of schools
- SAT 1250, ACT 27: Medium chance for 50% of schools
- SAT 1350, ACT 30: High chance for 50% of schools
- SAT 1250, ACT 28: Low chance for 75% of schools
- SAT 1350, ACT 30: Medium chance for 75% of schools
- SAT 1440, ACT 32: High chance for 75% of schools

For top schools and Ivy League schools:
- Top 5 schools (MIT etc): At least SAT 1470 or ACT 35
- Lower than 10% acceptanc rates
- Easiest Ivy League, Cornell University: At least SAT 1400 or ACT 32
- Cornell University 11% acceptance rate

For best non-Ivy colleges in each state:
- At least SAT 1296 or ACT 29

For "average" schools:
- Good chance for admittance: SAT 1250 or ACT 27
- Best chance for admittance: SAT 1350 or ACT 30

Correlations:
- Higher admission test scores, lower acceptance rates
- Acceptance rates lower as number of applicants increases
- Admission scores increase with number of applicants
- In general, schools require a higher ACT score than a SAT score for admission

### From dataset 2: SAT Scores by Intended College Major

Summary of statistics:
- Most test takers score higher on R&W section than Math section
- Average maximum score for all majors: 1242
- 75th percentile: 1116

College majors with highest/lowest scores from interested majors
- Scores for each section to aim for: Above R&W 597 and Math 646
- Recommended to score higher than these mean scores for a higher chance of acceptance into better schools

Correlations:
- Interested test takers who applied for popular majors generally do not have very high SAT scores
- Scores for R&W and Math sections are strongly correlated
- Most test takers did better on R&W as compared to Math

### Recommendations

### What SAT/ACT score should test takers aim for?

I recommend a range of scores for a new test taker to aim for SAT and ACT:

SAT **1300 - 1400**, ACT **29 - 32**

At 1400(SAT) or 32(ACT), a test taker unlocks a shot for Cornell University, an Ivy League school.

At 1300(SAT) or 29(ACT), the best non-Ivy schools in any state start to become available. Very good chance for any "average" schools.

Anywhere in between, the test taker would increase their chances for best non-Ivy schools in any state. These scores also ensure the test taker is above the rest when choosing any preferred college major.