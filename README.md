# RFM-Accounts-Segmentation-Analysis
**Task:** Divide subscribers from the database in Big Query into three segments (Lost, Top, Middle) using RFM analysis.

  ## **Stages of task completion:**

1. Write an SQL code to get a dataset for analysis that contains data:
   
visit_cnt - unique number of emails opened by account;
last_visit_date -  the date the letter was last opened;
revenue - will assume that on average we should have received $10 from each open user email.
  
   To analyze were taken only account_id  there was one open letter and last_visit_date ≠ null. 

2. Make a dictionary based on each RFM scale's particular meaning. You also need to look at the current state of affairs and divide each indicator into segments:

-How long has the user opened the last letter?
( Here you can take the last available date that has been released by all subscribers, so that you can count from it as long ago, a day, two ago).

-How many visits were there in total?

-How much money did we make from one user?

*The result:*  dashboard in  GoogleColab with an explanation of all its steps and an analysis of the results obtained



