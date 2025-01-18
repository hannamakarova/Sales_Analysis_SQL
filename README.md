# Sales_Analysis_SQL
In this project, I worked with an e-commerce database in BigQuery to analyze user account creation dynamics, email activity (sending, opening, and clicks), and user behavior in different categories. 
The goal was to generate insights that help assess user activity by country, segment users based on various parameters, and evaluate account verification status and subscription status.

Key Deliverables:
1. SQL Query Creation:
I created an SQL query to generate a dataset that includes key metrics for both accounts and emails.
The query calculates the following primary metrics:
Account Metrics: Number of accounts created.
Email Metrics: Number of emails sent, opened, and clicked.
Additionally, I calculated aggregate metrics to compare country performance:
Total by Country: Total number of accounts and emails by country.
Country Ranking: Ranking of countries based on the total number of accounts created and emails sent.

2. Data Grouping and Metrics:
The data was grouped by essential parameters such as:
Date: Account creation date for accounts, email send date for emails.
Country: The country of the users.
Send Interval: The sending interval set by the account.
Account Verification: Whether the account is verified or not.
Subscription Status: Whether the user unsubscribed from the service.
I used window functions to calculate rankings for countries based on account creation and email sending volume.

3. CTE (Common Table Expressions):
I used at least one CTE to modularize the query, making it easier to read and maintain. This helped structure the logic by separating different parts of the query, such as calculations for country-level aggregations and rankings.

4. UNION and Filtering:
To combine results for accounts and emails, I used the UNION operator.
I filtered the final results to only include the top 10 countries based on the rankings of account creation or email sending.

5. Looker Studio Visualization:
I created a visualization in Looker Studio to showcase the data for key metrics:
Account Count (account_cnt): Number of accounts created.
Total Emails Sent by Country (total_country_sent_cnt): Total number of emails sent by country.
Country Ranking for Accounts: Ranking of countries based on account creation.
Country Ranking for Emails: Ranking of countries based on emails sent.
The visualization also displays the email sending trend over time by plotting the sent_msg metric against the date.
