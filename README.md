i want to create a dashboard. I work in NIMHANS. and we have data from 6 cohorts. im trying to create this clickable thing where you hover your mouse over a grpah and it will say the sample size. we have 5 parameters, 3 sets of data

1. research EEG(1/2 timepoint)
2. clincial EEG (3 timepoints)
3. PSG 

in clinical EEG and PSG we have diagnosis

we want age and sex of participnat

maybe an age matched analysis would be nice.

there would be phase 1,2,3 (as in same participant may have come upto 3 times) - there has been repetitive data which can be seen in the excel

Exclude head circumference more than 61.

Combine sex and age together for analysis and perform age-matched analysis when comparing males and females.

The assessment_id consists of a 3-digit phase code followed by a 6-digit participant identifier. The first three digits indicate the phase and time point, and the last six digits represent the unique participant ID.

Phase structure:
If the assessment_id starts with 101 or 102, it is Phase 1 (baseline to 6 months).
If it starts with 111 or 112, it is Phase 2 (2 years to 2.5 years).
If it starts with 121 or 122, it is Phase 3 (4 years to 4.5 years).
If it starts with 131 or 132, it is Phase 4 (6 years to 6.5 years).

If a participant attends at 6 months, the ID starts with 102. The next 6-month visit follows the pattern 112, then 122, then 132. Even if a participant first appears at 102, this is still considered Phase 1.

Each participant can complete up to 5 cognitive assessments per visit. If a participant completes cognitive assessments but delays EEG until 6 months, the prefix changes accordingly (for example, to 102), but this still belongs to the correct phase grouping.

The last 6 digits represent the participant identity. If the 6-digit number appears only once, the participant attended once. If it appears multiple times, the participant attended multiple visits. For age distribution analysis, use only one entry per participant. For cap size analysis, do not remove repeated visits, as the goal is to examine cap usage frequency.

Ensure sex percentages are calculated using unique participants only.

For age distribution, either use only one phase per participant or create a bar graph where each phase is shown in a different color, since the same participant may appear across multiple years.

For cap size analysis, retain repeated participants to reflect real usage patterns.

Compare head circumference with another cohort, potentially a dementia cohort from the Indian subcontinent. Ensure this comparison is age-matched.

Create a dashboard that includes age distribution (unique participants), sex distribution (unique participants), phase distribution, cap size usage frequency, and head circumference comparison. Use a grid background and clear legends.

150 - schiz

130 - dementia

120 - Bipolar

comapre 2017 to date. during winters, do you see a particular group of patients coming in. help visualise and see. charts and graphs communicate more

if i clikc age group, i want to see how many females and males etc. I want to see males between age of 70-75, what are clinnical indications, want counts and percentages

now for the column names in the excel

adbs_no - 6-digit unique identifier

assessment_no - 9 digit, 3+ 6 digit unique identifier

sex

Age

128 - if it is 1 then it is yes, if it is 0 it is no

head_circumference
