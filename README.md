# Hypothesis-Testing---Independent-Project

## Background Information<br />
You work as a data scientist for the telecom operator Megatelco. The company offers its
clients two prepaid plans, Surf and Ultimate. The commercial department wants to know
which of the plans brings in more revenue in order to adjust the advertising budget.
You are going to carry out a preliminary analysis of the plans based on a relatively small
client selection. You'll have the data on 500 Megatelco clients: who the clients are, where
they're from, which plan they use, and the number of calls they made and text messages
they sent in 2018. Your job is to analyze clients' behavior and determine which prepaid
plan brings in more revenue.

## Description of the plans<br />
Megatelco rounds seconds up to minutes, and megabytes to gigabytes. For calls, each
individual call is rounded up: even if the call lasted just one second, it will be counted as
one minute. For web traffic, individual web sessions are not rounded up. Instead, the
total for the month is rounded up. If someone uses 1025 megabytes this month, they will
be charged for 2 gigabytes.

      ### Surf
            1. Monthly charge: $20
            2. 500 monthly minutes, 50 texts, and 15 GB of data
            3. After exceeding the package limits:
                  ○ 1 minute: 3 cents
                  ○ 1 text message: 3 cents
                  ○ 1 GB of data: $10

      ### Ultimate
            1. Monthly charge: $70
            2. 3000 monthly minutes, 1000 text messages, and 30 GB of data
            3. After exceeding the package limits:
                  ○ 1 minute: 1 cent
                  ○ 1 text message: 1 cent
                  ○ 1 GB of data: $7

## Instructions on completing the project
##### Step 1. Open the data file and study the general information<br />
● Download Link: https://bit.ly/3lrTn9z<br />
##### Step 2. Prepare the data<br />
● Convert the data to the necessary types<br />
● Find and eliminate errors in the data<br />
■ Explain what errors you found and how you removed them.

For each user, find:<br />
● The number of calls made and minutes used per month<br />
● The number of text messages sent per month<br />
● The volume of data per month<br />
● The monthly revenue from each user (subtract the free package limit from the
total number of calls, text messages, and data; multiply the result by the calling
plan value; add the monthly charge depending on the calling plan)<br />
##### Step 3. Analyze the data<br />
● Describe the customers' behavior. Find the minutes, texts, and volume of data
the users of each plan require per month. Calculate the mean, variance, and
standard deviation. Plot histograms. Describe the distributions.<br />
##### Step 4. Test the hypotheses<br />
● The average revenue from users of Ultimate and Surf calling plans differs.<br />
● The average revenue from users in NY-NJ area is different from that of the users
from other regions.<br />

You decide what alpha value to use.<br />
Explain:<br />
● How you formulated the null and alternative hypotheses.<br />
● What criterion you used to test the hypotheses and why.<br />
Step 5. Write an overall conclusion<br />
● Format: Complete the task in Google Colab. Put the programming code in code
cells and text explanations in markdown cells, then apply formatting and
headings.<br />

## Description of the data<br />
###### The users table (data on users):
● user_id — unique user identifier<br />
● first_name — user's name<br />
● last_name — user's last name<br />
● age — user's age (years)<br />
● reg_date — subscription date (dd, mm, yy)<br />
● churn_date — the date the user stopped using the service (if the value is
missing, the calling plan was being used when this database was extracted)<br />
● city — user's city of residence<br />
● plan — calling plan name<br />

###### The calls table (data on calls):<br />
● id — unique call identifier<br />
● call_date — call date<br />
● duration — call duration (in minutes)<br />
● user_id — the identifier of the user making the call

###### The messages table (data on texts):<br />
● id — unique text message identifier<br />
● message_date — text message date<br />
● user_id — the identifier of the user sending the text<br />

###### The internet table (data on web sessions):<br />
● id — unique session identifier<br />
● mb_used — the volume of data spent during the session (in megabytes)<br />
● session_date — web session date<br />
● user_id — user identifier<br />

###### The plans table (data on the plans):<br />
● plan_name — calling plan name<br />
● usd_monthly_fee — monthly charge in US dollars<br />
● minutes_included — monthly minute allowance<br />
● messages_included — monthly text allowance<br />
● mb_per_month_included — data volume allowance (in megabytes)<br />
● usd_per_minute — price per minute after exceeding the package limits (e.g., if
the package includes 100 minutes, the 101st minute will be charged)<br />
● usd_per_message — price per text after exceeding the package limits<br />
● usd_per_gb — price per extra gigabyte of data after exceeding the package limits
(1 GB = 1024 megabytes)
