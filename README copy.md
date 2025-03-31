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
- Numbered ordered notebooks (.ipynb)
    - 1. Loads the data provided for the case and goes through cleaning operations before storing in db 
        - Table name:
    - 1.1 Lists out data quality points noticed in the data, need to follow up with data provider for more details 
        - Small in number so mostly ignored but could also remove from data analysis 
    - 2. Loads in the cleaned data table saved from process 1 and creates additional columns that could be useful in data tables (should start working on this in parallel with 4) - save in same db
    - 3. Loads in cleaned metric infused data from process 2 and creates a clean group by view as well as appends any grouped metrics before saving in db
    - 4. Run majority visualizations and analysis for the purpose of report

- Subscriptions db (.db)
    - Contains the following tables 
        - Cleaned user level data generated from notebook process 1
        - Metric infused user level data from notebook process 2
        - Metric infused group by table from notebook process 3

- Write up PDF
    - Summary of my findings synthesized into a report

## Future Improvements
- Add a fifth notebook file for predictions 
    - LTV, overall portfolio forecasting of revenue 
- Clean up the visualizations_tables code to be more efficient and succint, can also move some of the calculated fields into the grouped_views process 3 notebook. 
- Try more creative ways to utilize the snapshot view to capture revenue retention and growth 
- Follow up with data quality points and devise better ways to address if no further information is given
