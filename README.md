# Retention Analysis Exercise

## Goal
The goal of this exercise is to gain an understanding of the retention characteristics of a subscription product, using code and data.

Potential analysis may include but are not limited to
- How is retention trending for different starting cohorts?
- How does customer retention compare with revenue retention? 
- Is there evidence of revenue expansion at the customer level?
- How does retention vary by geography? or provider?

## Data
The provided `dummy_customer_file` has the following schema

- `oid`: customer id
- `provider`: payment platform
- `total_charges`: total revenue collected to date
- `signup_date`: date of first sign up (could be sign up to free trial)
- `is_canceled`: is the paid plan cancelled
- `is_active`: is the paid plan active
- `is_delinquent`: is the user late on payment
- `conversion_date`: date of conversion to paid plan
- `cancellation_date`: date of the cancellation
- `current_mrr`: effective monthly subscription fee
- `personal_person_geo_country`: country of the user
- `converted`: has the user converted to paid plan

Note that there may be data type inconsistencies, e.g. some columns are dates and some are timestamps, and value inconsistencies, e.g. country values are not standardized. Please account for these appropriately in your analysis

## Output specification
This is meant to be an open ended exercise, so how you decide tackle it is up to you. However, here are some high level guideline that you should follow
- please use code (e.g. Python) and not a spreadsheet for the analysis
- provide a synthesis that contains an assessment of the retention characteristics of the product
- support your synthesis with charts based on the data provided

The final deliverable should include your code and your synthesis