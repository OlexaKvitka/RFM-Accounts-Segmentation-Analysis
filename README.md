# RFM-Accounts-Segmentation-Analysis
Task: Divide subscribers from the database in Big Query into three segments (Lost, Top, Middle) using RFM analysis.

  Stages of task completion:

Write an SQL code to get a dataset for analysis that contains data:
visit_cnt - unique number of emails opened by account;
last_visit_date -  the date the letter was last opened;
revenue - will assume that on average we should have received $10 from each open user email.
   To analyze were taken only account_id  there was one open letter and last_visit_date ≠ null. 


Resulting  SQL code

SELECT
 id as account_id,
 COUNT(DISTINCT ev.id_message) as visit_cnt,
 MAX(DATE_ADD(s.date, INTERVAL eo.open_date DAY)) as last_visit_date,
 COUNT(DISTINCT eo.id_message)*10 as revenue
from `DA.account` as a
left join `DA.email_open` eo
on a.id=eo.id_account
left join `DA.email_visit` as ev
on a.id=ev.id_account
Left JOIN `DA.account_session` as acs
on a.id=acs.account_id
left join `DA.session` s
on acs.ga_session_id=s.ga_session_id
GROUP BY account_id
having visit_cnt>0 and last_visit_date is not null

2. Make a dictionary based on each RFM scale's particular meaning. You also need to look at the current state of affairs and divide each indicator into segments:

-How long has the user opened the last letter?
( Here you can take the last available date that has been released by all subscribers, so that you can count from it as long ago, a day, two ago).

-How many visits were there in total?

-How much money did we make from one user?

The result:  dashboard in  GoogleColab with an explanation of all its steps and an analysis of the results obtained:



