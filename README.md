# AB-test
Evaluation of the A/B test results for a landing page.
See file ABtest_v1.ipynb

## Problem statement

Business goal: to increase income via a landing page promoting  purchases.

Metrics preset by a customer:
 - Conversion (a ratio of number of purchases to number of visits, %)
 - Mean bill ( a ratio of total income to number of purchases, USD)


## Data
A single .csv file with the following columns:
- user_id - personal identifier for every user visiting the page;
- date ;
- group - a testing group: A or B;
- purchase - a binary attribute if a purchase was made;
- price - purchase sum.

The next products for purchase are available:
- USD 10;
- USD 60;
- USD 100;
- USD 150;
- USD 200.

Specific feature: in one session, only one product may be purchased.

## Approach 
Statistical significance for conversion difference was estimated with a z-test for proportions.
Additionally, confidence intervals  (CI) for conversions and their difference were estimated.

Statistical significance for difference in mean bills between groups was estimated with a t-test.
Additionally, confidence intervals  (CI) for conversions and their difference were estimated.

## Results
By conversion, groups A and B do not differ significantly. 
But the main bill (among users who made a purchase) is significantly different: in group B it is 10% greater than in group A.
The recommendation for a business customer is to provide deeper business analysis and change metrics. I would recommend to use a metrics of another "mean bill": total income divided by a total number of page visitors, therefore the effect of the landing page design is accounted in a more integrated way: both the number of buyers and their expenses are considered.

