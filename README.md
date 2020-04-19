# Project 1: Analysis on SAT and ACT Participation and Performance in United States

### Problem Statement
The ACT has long claimed the title as the most widely used college admission assessment in United States since 2012 [[Source: Washington Post, 2018]](https://www.washingtonpost.com/education/2018/10/23/sat-reclaims-title-most-widely-used-college-admission-test/). Many states have enacted law to mandate ACT as the default assessment for high school graduates, giving rise to the popularity of ACT, taking over SAT. Thus for the College Board, it would be quintessential to understand the reason behind ACT long-lasting popularity and formulate a cost-efficient solution to improve the SAT participation rate.

---

### Executive Summary
In March 2016, a new format of Standardized Test (SAT) was released by its adminstrative and management body, the College Board. The format changes was aimed to promote higher participation rate in the assessment. David Coleman, president of the College Board, commented that the SAT was seen by the public “narrowly as a test for advanced kids.” [[Source: Washington Post, 2018]](https://www.washingtonpost.com/education/2018/10/23/sat-reclaims-title-most-widely-used-college-admission-test/). It was revered for its design emphasis on critical thinking and robust vocabulary, a hallmark that shy away the general public.

Henceforth, the College Board has decided to simplify the assessment design — from the original 10 sections down to 5 [[Source: College Board, n.d.]](https://collegereadiness.collegeboard.org/sat/inside-the-test/compare-old-new-specifications). Every component of the SAT, including the essay, has a new format and a shift in the skills it focuses on, in the hope of encouranging influx of participants from its rival, American College Testing (ACT).

In this project, we will dive into the SAT and ACT data in the year 2017 and 2018, which detailed state-wide average participation rate and the assessments' corresponding subject scores to unravel any statistical relationship between the variables. The relationship and distribution are visualized to reveal patterns that could show details that would otherwise stayed unseen. Upon understanding the statistical relationship, we will then zoom into some states to understand the effect of policy changes that has affected the participation rate or public sentiments towards the SAT. From which, we would devise the proven, most cost-effective recommendation to improve the participation rate of SAT in the United States.

The data were sourced from statistics available online, which were then converted into table (csv) format for the ease of data transformation and analysis. The sources are as followed:

1. [SAT 2017](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/)
2. [ACT 2017](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows)
3. [SAT 2018](https://reports.collegeboard.org/sat-suite-program-results/state-results)
4. [ACT 2018](http://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf)

These data give average SAT and ACT scores by state, as well as participation rates, for the graduating class of 2017 and 2018. You may refer to the data dictionary below for details on each variable:

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|_object_|All|All 50 states in the U.S. and Washington D.C.|
|**sat_participation_2017**|_integer_|SAT 2017|Student participation rate for SAT in each states in 2017 (units percent to zero decimal places 98 means 98%)|
|**sat_reading_writing_2017**|_integer_|SAT 2017|State-average evidence-based reading and writing score in 2017 (units score range from 200 to 800)|
|**sat_math_2017**|_integer_|SAT 2017|State-average mathematics score in 2017 (units score range from 200 to 800)|
|**sat_total_2017**|_integer_|SAT 2017|State-average total score in 2017 (units score range from 400 to 1600)|
|**act_participation_2017**|_integer_|ACT 2017|Student participation rate for ACT in each states in 2017 (units percent to zero decimal places 98 means 98%)|
|**act_english_2017**|_float_|ACT 2017|State-average evidence-based reading and writing score in 2017 (units score to one decimal places range from 1.0 to 36.0)|
|**act_math_2017**|_float_|ACT 2017|State-average mathematics score in 2017 (units score to one decimal places range from 1.0 to 36.0)|
|**act_reading_2017**|_float_|ACT 2017|State-average reading score in 2017 (units score to one decimal places range from 1.0 to 36.0)|
|**act_science_2017**|_float_|ACT 2017|State-average mathematics score in 2017 (units score to one decimal places range from 1.0 to 36.0)|
|**act_composite_2017**|_float_|ACT 2017|State-average composite score in 2017 (units score to one decimal places range from 1.0 to 36.0)|
|**sat_participation_2018**|_integer_|SAT 2018|Student participation rate for SAT in each states in 2018 (units percent to zero decimal places 98 means 98%)|
|**sat_reading_writing_2018**|_integer_|SAT 2018|State-average evidence-based reading and writing score in 2018 (units score range from 200 to 800)|
|**sat_math_2018**|_integer_|SAT 2018|State-average mathematics score in 2018 (units score range from 200 to 800)|
|**sat_total_2018**|_integer_|SAT 2018|State-average total score in 2018 (units score range from 400 to 1600)|
|**act_participation_2018**|_integer_|ACT 2018|Student participation rate for ACT in each states in 2018 (units percent to zero decimal places 98 means 98%)|
|**act_english_2018**|_float_|ACT 2018|State-average evidence-based reading and writing score in 2018 (units score to one decimal places range from 1.0 to 36.0)|
|**act_math_2018**|_float_|ACT 2018|State-average mathematics score in 2018 (units score to one decimal places range from 1.0 to 36.0)|
|**act_reading_2018**|_float_|ACT 2018|State-average reading score in 2018 (units score to one decimal places range from 1.0 to 36.0)|
|**act_science_2018**|_float_|ACT 2018|State-average mathematics score in 2018 (units score to one decimal places range from 1.0 to 36.0)|
|**act_composite_2018**|_float_|ACT 2018|State-average composite score in 2018 (units score to one decimal places range from 1.0 to 36.0)|

---

### Conclusion/Recommendation
If we look into states where it is not 'monopolized' by ACT, there are 4 states - West Virginia, Arizona, Florida and Hawaii - that has lower SAT participation rate but still relatively neutral on its stance (or rather, policy) on ACT vs SAT. These states would be easier to be converted than others, none of these 4 states have policy that is favourable towards ACT. 

But if we would to only target at a single state to promote SAT, West Virginia would be the best candidate. West Virginia has already gained momentum from the SAT School Day Programme that allows student to participate in the assessment for free and during a school day (instead of Weekends). The most cost-effective method to improve the SAT participation rate in West Virginia would be to organize state-wide campaign promoting the School Day Programme, so we may fully utilize the momentum we have created by investing in the programme. The participation would certainly be improved when the high school juniors are more well-informed of the programme that comes at zero cost and held on an usual school day.

However, once the effect of the School Day Programme has plateaued, the College Board may look into options to negotiate with the state government for long term support and contract to make SAT mandatory state-wide. This method would have a higher cost impact, but considering West Virginia has a relatively low population count (39th place out of 50 states in U.S.), the cost would be relatively lower than most of the states (such as Illinois or Colorado) that has implemented such contract.