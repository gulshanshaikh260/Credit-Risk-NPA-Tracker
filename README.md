#  Credit Risk & NPA Delinquency Tracker

##  Objective
This project connects customer loan profiles with EMI repayment histories to dynamically track delinquencies and automatically classify Non-Performing Assets (NPAs).

##  Technical Skills Demonstrated

Relational Database Design: Building and seeding tables with precise financial data types (e.g., DECIMAL(12,2) to handle large-scale home loan disbursements).

Advanced Joins & Aggregations: Utilizing INNER JOIN, SUM(), and MAX() across simulated banking data to connect static loan profiles with dynamic, multi-row payment ledgers.

Conditional Risk Logic: Applying aggregated CASE WHEN statements to evaluate worst-case payment delays and trigger automated risk flags.

##  The Audit Logic
The master query (02_npa_delinquency_audit.sql) evaluates raw retail banking data to output an executive-level risk report:

Ledger Aggregation: Calculates Total EMI Paid per loan dynamically.

Delinquency Tracking: Identifies the maximum Days_Past_Due for each account's payment history.

Asset Classification: Automatically classifies the loan as an NPA (Non-Performing Asset) if the default threshold strictly exceeds 90 days, otherwise classifying it as a Standard asset.
