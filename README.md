# Financial-Service

Variable Descriptions and Use in Segmentation

Column	Meaning	Use in Segmentation
issue_d	Loan issuance date	Can be used for cohort analysis (e.g., customers in 2014 vs. 2018)
sub_grade	Risk level within loan grade (e.g., A1 to G5)	Proxy for creditworthiness – lower grades = higher risk
term	Loan duration (36 or 60 months)	Segment by product type preference or risk exposure
home_ownership	Ownership status (e.g., RENT, MORTGAGE, OWN)	Reflects stability or asset ownership
fico_range_low	FICO score (low end of range)	Key indicator of credit risk
total_acc	Total number of credit accounts	Higher values suggest more credit experience
pub_rec	Number of derogatory public records	Indicator of financial missteps (e.g., bankruptcies)
revol_util	Revolving credit utilization rate	Higher = more leveraged; a credit risk signal
annual_inc	Stated annual income	Can segment based on income brackets
int_rate	Interest rate on loan	Higher = more risky borrowers or lower credit
dti	Debt-to-income ratio	Measures ability to handle monthly debt
purpose	Reason for loan (e.g., credit_card, debt_consolidation)	Segment by financial need or goal
mort_acc	Number of mortgage accounts	Additional financial responsibility indicator
loan_amnt	Amount funded by investors	Segment by small vs. large loan size
application_type	Individual or joint loan application	Joint may suggest higher household income
installment	Monthly repayment amount	Indicator of borrower’s payment burden
verification_status	Income verification status	Segment by credibility: Verified vs. Not Verified
pub_rec_bankruptcies	Past bankruptcies	Indicator of default risk
addr_state	US state of residence	Use for geo-segmentation or regional trends
initial_list_status	Publicly listed (w) or privately listed (f)	Less relevant; minor segment flag
fico_range_high	FICO score (high end of range)	Complement to fico_range_low
revol_bal	Revolving credit balance	Total balance on lines of credit
id	Unique loan ID	For internal use only, not used in segmentation
open_acc	Number of open credit lines	Higher values suggest more financial activity
emp_length	Employment length in years (1–10+, or NA)	Indicator of income stability
loan_status	Loan outcome (e.g., Fully Paid, Charged Off)	Label for supervised learning, or outcome grouping
time_to_earliest_cr_line	Time since first credit line	Proxy for credit history length
