OTT-User-Retention-Dashboard-using-power-bi

## Overview

Power BI dashboard project to analyze user engagement, retention, and churn behavior in an OTT streaming platform.



# Tools Used

* Power BI
* DAX
* Power Query



# Key KPIs

* Total Users
* Churned Users
* Churn Rate
  

#DAX measure

1.Total Users
Total Users =
DISTINCTCOUNT(synthetic_ott_user_activity[user_id])

2.Retained Users
Retained Users =
CALCULATE(
COUNT(synthetic_ott_user_activity[user_id]),
synthetic_ott_user_activity[churned] = 0
)

3.Churned Users
Churned Users =
CALCULATE(
COUNT(synthetic_ott_user_activity[user_id]),
synthetic_ott_user_activity[churned] = 1
)

4.Retention Rate
Retention Rate =
DIVIDE([Retained Users],[Total Users]) * 100

5.Churn Rate
Churn Rate =
DIVIDE([Churned Users],[Total Users]) * 100

# Dashboard Pages

1. Executive Overview
2. User Engagement Dashboard
3. Retention Dashboard
4. User Performance Dashboard



# Key Insights

* Premium users showed higher retention.
* Higher watch time reduced churn.
* Mobile users had strong engagement.
* Some regions showed higher churn.


# Conclusion

The dashboard helps analyze OTT user behavior and provides insights to improve customer retention and engagement.
