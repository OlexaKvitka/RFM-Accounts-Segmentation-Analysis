# RFM-Accounts-Segmentation-Analysis

**TASK**: Divide subscribers from the database in Big Query into three segments (Lost, Top, Middle) using RFM analysis in Google Colab

## Deliverables  
-  [Google Colab Notebook:](https://colab.research.google.com/drive/16QhFxl1e64_8TIzCXdUIBRPSZdDxS7Lo?usp=sharing#scrollTo=M3bUrqPoiFq6)
 
## Google Colab Notebook Preview:
![RFM Accounts Segmentation Analysis](https://github.com/OlexaKvitka/RFM-Accounts-Segmentation-Analysis/blob/main/RFM%20Accounts%20Segmentation%20Analysis.PNG)

## **Stages of task completion:**

*1. Write an SQL code to get a dataset for analysis that contains data:*
   
visit_cnt - unique number of emails opened by account;
last_visit_date -  the date the letter was last opened;
revenue - will assume that on average we should have received $10 from each open user email.

   To analyze were taken only account_id  there was one open letter and last_visit_date ≠ null. 
*2. Make a dictionary based on each RFM scale's particular meaning.*

It's also need to look at the current state of affairs and divide each indicator into segments:

-How long has the user opened the last letter?
(I took the last available date that has been released by all subscribers, so that permit to count from it as long ago, a day, two ago).

-How many visits were there in total?

-How much money did we make from one user?

 ## Google Colab Part Structure
 
-Load data
-Calculate RFM metrics
-Create RFM scores (1-4)
-Segmentation (Top/Middle/Lost)
-Segment analysis
-Visualization
-Business Impact & Recommendations

## Segment Analysis KEY Observations
Analysis of 4,463 email subscribers reveals three distinct engagement tiers. The Top segment (36%) demonstrates strong engagement patterns, while a significant portion (21%) shows signs of disengagement requiring immediate intervention.

*Segment Distribution:*
    Top: 1,612 subscribers (36.1%)
    Middle: 1,900 subscribers (42.6%)
    Lost: 951 subscribers (21.3%)
    Top Subscribers (36.1%)

**High-value segment contributing $916,640 in total revenue:**

Recency: 39 days (recently active)
Frequency: 8.6 opens (highly engaged)
Monetary: $569 average per subscriber
Revenue contribution: 63% of total
Middle Subscribers (42.6%)

**Moderate engagement with growth potential, contributing $478,000:**

Recency: 56 days (moderate activity)
Frequency: 2.9 opens (occasional engagement)
Monetary: $252 average per subscriber
Revenue contribution: 33% of total
Lost Subscribers (21.3%)

**At-risk segment showing minimal engagement, contributing $56,970:**

Recency: 77 days (inactive)
Frequency: 1.4 opens (minimal engagement)
Monetary: $60 average per subscriber
Revenue contribution: 4% of total

## Business Impact & Recommendations
The subscriber base demonstrates strong engagement (79% active), with revenue heavily concentrated in the Top segment (63% from 36% of subscribers). Strategic focus should prioritize preventing Middle segment churn, maximizing Top segment value, and systematic Lost subscriber reactivation.

**Strategic Actions by Segment**

*Top Segment (36%): Retention & Growth*

-Launch VIP program with exclusive content and early product access
-Implement referral incentives to acquire similar high-value subscribers
-Deploy A/B testing on premium content formats
-Monitor engagement decay signals for early intervention
 
 **Middle Segment (43%): Activation & Upgrade**

-Deploy triggered email sequences based on behavior patterns
-Test personalized content and optimal send frequency
-Map conversion path from Middle to Top with milestone incentives
-Implement progressive profiling for enhanced targeting

**Lost Segment (21%): Reactivation & Hygiene**

-Execute 3-5 email win-back series over 30 days
-Survey disengagement reasons and analyze drop-off patterns
-Implement sunset policy for 90+ day non-responders
-Prioritize recovery efforts by historical subscriber value

The current subscriber base shows healthy engagement from 79% of the list, with significant revenue concentration in the Top segment. Strategic priorities should focus on preventing Middle segment churn, maximizing Top segment lifetime value, and implementing systematic reactivation efforts for Lost subscribers.

Early intervention at the 60-day recency threshold presents the highest ROI opportunity for maintaining list health and revenue growth.

