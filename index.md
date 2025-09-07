---
layout: default
title: Home
---


<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Term Deposit Marketing Campaign</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Term Deposit Marketing Campaign</h1>

  <section>
    <h2>Executive Summary</h2>
    <p>
      Bank A’s marketing campaign, conducted primarily through phone calls, sought to increase subscriptions to its term deposits. 
      Overall, customer demographics, financial standing, and the quality of campaign interactions strongly influence subscription rates.
    </p>
    <p>Analysis of the dataset revealed the following key insights:</p>

    <figure style="margin:20px; max-width:600px; text-align:left;">
      <img src="images/1.Overview.png" 
          alt="Data Insights" 
          style="width:100%; display:block;">
      <figcaption style="font-size:0.9em; color:#555; margin-top:8px;">
        Figure 1: Overview
      </figcaption>
    </figure>


    <ul>
      <li>Subscriber Composition: Only 11.52% of customers subscribed, showing strong untapped potential.</li>
      <li>Demographics: Subscriptions are concentrated in the 30–40 age group, who also hold higher average yearly balances. Clients under 30 show low subscription rates.</li>
      <li>Occupational Profile: Managers, technicians, and blue-collar workers are the main subscriber groups, suggesting campaign tailoring to specific work environments.</li>
      <li>Campaign Effectiveness: Longer calls reduce the need for follow-ups, highlighting the importance of quality over quantity in customer engagement.</li>
      <li>Clustering Insights: K-means clustering identified promising customer segments, particularly blue-collar and technician workers with secondary education and clients aged 38–43.</li>
      <li>Predictive Analytics: Decision trees and regression models showed that call duration, prior campaign outcomes, and occupation are the strongest predictors of subscription likelihood.</li>
      <li>Prescriptive Analytics: Monte Carlo simulation suggests that optimizing parameters such as call duration, campaign frequency, and personalized incentives can maximize expected subscriptions.</li>
    </ul>
  </section>



  <section>
    <h2>Introduction</h2>
    <p>
      Bank A conducted a phone-based marketing campaign to promote its term deposit products. 
    </p>
    <p>The dataset contains:</p>
    <ul>
      <li>Demographics: age, marital status, employment status, etc.</li>
      <li>Bank-related data: client financial and account information.</li>
      <li>Campaign interaction details: call duration, number of calls per client.</li>
      <li>Outcome: whether the client subscribed to the term deposit.</li>
    </ul>
    <p>This dataset enables analysis of client characteristics, campaign effectiveness, and factors influencing subscription decisions.</p>
  </section>

  <section>
    <h2>Situation</h2>
    <p>
      The marketing campaign mainly via phone calls aimed to boost term deposit subscriptions but resulted in varied outcomes.
    </p>
  </section>

  <section>
    <h2>Complication</h2>
    <p>
      Success rate of the existing phone call approach is uncertain. Various investment options such as cryptocurrency, stock market, annuity plan, etc 
      make the bank exercise more campaigns to attract customers to consider term deposits.
    </p>
  </section>

  <section>
    <h2>Business Problem</h2>
    <p>
      What customer characteristics / segments contribute to a higher likelihood of subscribing to term deposits?
    </p>
    <p>
      Variables include demographic (age, marital status, and occupation), bank information (bank balance, housing loans, and personal loans), and campaign information (duration of calls, number of calls, and previous campaign outcomes).
    </p>
    <p>
      Assumptions include that customer demographic and financial standing remain unchanged, the external market environment stays stable, and no disruptive events such as crises or new competitors occur during the forecast period.
    </p>
  </section>

  <section>
    <h2>Dataset Summary</h2>
    <p>Key variables in the dataset:</p>
    <table>
      <tr><th>Field</th><th>Type</th><th>Description</th></tr>
      <tr><td>age</td><td>Ratio</td><td>Current age</td></tr>
      <tr><td>job</td><td>Nominal</td><td>Occupation</td></tr>
      <tr><td>marital</td><td>Nominal</td><td>Marital status</td></tr>
      <tr><td>education</td><td>Ordinal</td><td>Education level</td></tr>
      <tr><td>balance</td><td>Ratio</td><td>Average yearly balance</td></tr>
      <tr><td>housing</td><td>Nominal</td><td>Housing loan</td></tr>
      <tr><td>personal</td><td>Nominal</td><td>Personal loan</td></tr>
      <tr><td>contact</td><td>Nominal</td><td>Channel of contact</td></tr>
      <tr><td>duration</td><td>Ratio</td><td>Duration of last contact</td></tr>
      <tr><td>campaign</td><td>Ratio</td><td>No. of contacts in current campaign</td></tr>
      <tr><td>previous</td><td>Ratio</td><td>No. of contacts prior to campaign</td></tr>
      <tr><td>poutcome</td><td>Nominal</td><td>Previous campaign outcome</td></tr>
      <tr><td>deposit</td><td>Nominal</td><td>Subscribed to deposit (Yes/No)</td></tr>
    </table>
    
    <figcaption style="font-size:0.9em; color:#555; margin-top:8px;">
        Figure 2: Dataset
      </figcaption>

  </section>

  <section>
    <h2>Dashboard Visualisation via PowerBI</h2>

    <img src="images/3.Dashboard.png" 
      alt="Dashboard" 
      style="width:100%; max-width:600px; display:block; margin:20px;  text-align:left;">
    <figcaption style="font-size:0.9em; color:#555; margin-top:8px;">
        Figure 3: Dashboard
      </figcaption>
  </section>

  <section>
    <h2>Visual Insights</h2>
    <h3>Subscribers vs Non-Subscribers</h3>

    <img src="images/4.Piechart - Subscribers vs Non-Subscribers.png" 
      alt="Piechart - Subscribers vs Non-Subscribers" 
      style="width:100%; max-width:600px; display:block; margin:20px;  text-align:left;">
    <figcaption style="font-size:0.9em; color:#555; margin-top:8px;">
        Figure 4: Subscribers vs Non-Subscribers
      </figcaption>
  </section>


    <p>Pie Chart is used to display proportions of deposit subscribers vs. non-subscribers. Only 11.52% of customers subscribed to term deposits, indicating significant potential for growth.</p>

    <h3>Age Groups & Average Balance</h3>

    <img src="images/5.Histogram - Age Groups & Average Balance.png" 
      alt="Histogram - Age Groups & Average Balance" 
      style="width:100%; max-width:600px; display:block; margin:20px;  text-align:left;">
    <figcaption style="font-size:0.9em; color:#555; margin-top:8px;">
        Figure 5: Age Groups & Average Balance
      </figcaption>
  </section>
    <p>
    A histogram is used to visualize the age distribution among clients, identifying age groups with higher or lower subscription rates, suggesting potential strategies for different age group. The bar chart also shows average yearly balance balances which are available for term deposit among age group.
    </p>
    <p>
    A positively skewed distribution suggests that the data is concentrated on one side of the scale (Taylor, 2024). The skewness indicates a small number of subscribers under 30, while the age group between early 30s and early 40s holds higher average yearly balance. Bank A can develop marketing strategies to target this age group for term deposit subscriptions.
    </p>

    <h3>Job Composition</h3>
    
    <img src="images/6.Stacked bar - Job Composition.png" 
      alt="Stacked bar - Job Composition" 
      style="width:100%; max-width:600px; display:block; margin:20px;  text-align:left;">
    <figcaption style="font-size:0.9em; color:#555; margin-top:8px;">
        Figure 6: Job Composition
      </figcaption>
    <p>
    A stacked bar chart is used to show job composition The primary deposit subscribers hold management positions, followed by technicians and blue-collar workers. Therefore, relevant marketing campaigns, such as roadshows, can be organized at operational sites and offices to target technicians and blue-collar workers, and managers respectively
    </p>

    <h3>Call Duration & Effectiveness</h3>

    <img src="images/7.Bubble Chart - Call Duration & Effectiveness.png" 
      alt="Bubble Chart - Call Duration & Effectiveness" 
      style="width:100%; max-width:600px; display:block; margin:20px;  text-align:left;">
    <figcaption style="font-size:0.9em; color:#555; margin-top:8px;">
        Figure 7: Call Duration & Effectiveness
      </figcaption>
    <p>
    A bubble chart is used to visualize the relationship among three dimensions last contact duration, total contacts made during this campaign and deposit subscriber vs non-subscriber, whereas a scatter chart displays only two value axes. (Pedamkar, 2023). It also uses to assess the effectiveness of the marketing campaign.
    </p>
    <p>
    A negative correlation between the last contact duration and number of contacts performed during current campaign, suggesting that longer conversations lead to fewer follow-ups. It may reflect a strategic shift in approach, where quality interactions are prioritized over quantity, leading to more in-depth discussions rather than multiple brief contacts. The effectiveness of campaign is not necessary to have long duration of call.
    </p>

  </section>

  <section>
    <h2>Business Analytics Solution via Machine Learning</h2>
    
    <h3>Clustering</h3>
    <p>Clustering groups customers into segments based on similar characteristics, facilitating targeted marketing efforts. K-means clustering can categorize clients into distinct groups based on demographic (age, marital status, and occupation), financial status (bank balance, housing loans, and personal loans) and responses to campaign (duration of calls, number of calls, and previous campaign outcomes). The dataset is filtered for "Deposit" = "Yes" to identify customers who subscribed to the term deposit. Load the data into the machine, specifying the input variables and the value of "K," or the number of clusters. The machine will compute K centroids, and each data point will be assigned to its nearest centroid.</p>
    
    <img src="images/8.Clustering.png" 
      alt="Clustering" 
      style="width:100%; max-width:600px; display:block; margin:20px;  text-align:left;">
      <figcaption style="font-size:0.9em; color:#555; margin-top:8px;">
        Figure 8: Clustering by customer profiles
      </figcaption>

    <p>The bank can refine the marketing strategies, focusing on group of customers from blue-collar, technician with secondary school education and also customers in age group between 38 years old and 43 years old.</p>
    
    <h3>Predictive Modeling</h3>
    <p>The bank can apply a predictive modelling namely, regression, neural networks and decision trees to estimate probabilities of customer subscribing to a term deposit as a target outcome (“deposit”) based on criteria of customers’ social demographic status (age, marital status, and occupation), financial status (bank balance, housing loans, and personal loans) and responses to campaign (duration of calls, number of calls, and previous campaign outcomes) as the input variables. The target output is the Deposit" = "Yes". (Banu, 2023) The classification algorithm is trained on historical data and its performance is validated via cross-validation method. The anticipated outcome will be displayed in a decision tree, where each observation is allocated to a leaf node with a binary result: "Yes" for subscribe and "No" for not subscribe. The splitting criteria include demographic status, financial status and responses to campaign. The predictive model’s accuracy can measure using metrics such as Mean Square Error, F1-score ,accuracy, precision and recall (Koh, 2005)</p>
    
    <img src="images/9.Classification and Regression Trees (CART) for Deposit.png" 
      alt="Classification and Regression Trees (CART) for Deposit" 
      style="width:100%; max-width:600px; display:block; margin:20px;  text-align:left;">
    <figcaption style="font-size:0.9em; color:#555; margin-top:8px;">
        Figure 9: Classification and Regression Trees (CART) for Deposit
      </figcaption>
    
    <p>Inputs higher in the decision tree i.e. duration of last contact, outcome of the previous marketing campaign (e.g., success, failure, unknown), job are considered more influential for predicting the target customers subscribing deposit.</p>
    
    <h3>Prescriptive Analytics</h3>
    <p>Prescriptive analytics e.g. Monte Carlo Simulation can be used to create numerous simulated scenarios by randomly varying input parameters (e.g., call duration, campaign frequency, offer incentives). For each scenario, assess the predicted probability of subscription and calculate the expected number of conversions. Monte Carlo Simulation allows the bank to provide personalized messaging at scale and increase the chance of yielding the highest expected number of subscribing the term deposit.</p>
  </section>

  <section>
    <h2>Recommendations & Next Steps</h2>
    <h3>1. Targeted Campaigns</h3>
    <ul>
      <li>Focus on 30–43 age group with higher balances.</li>
      <li>Tailor marketing approaches for managers, technicians, and blue-collar workers, including workplace campaigns and financial education sessions.</li>
    </ul>
    <h3>2. Improve Call Strategy</h3>
    <ul>
      <li>Train agents to prioritize longer, more meaningful conversations instead of multiple short follow-ups.</li>
      <li>Use predictive analytics to identify high-potential customers before outreach.</li>
    </ul>
    <h3>3. Segmented Incentives</h3>
    <ul>
      <li>Implement decision tree models in CRM systems to provide real-time guidance to agents on customer subscription likelihood.</li>
    </ul>
    <h3>4. Leverage Predictive Models</h3>
    <ul>
      <li>Integrate decision trees in CRM for real-time guidance.</li>
    </ul>
    <h3>5. Run Prescriptive Simulations</h3>
    <ul>
      <li>Use Monte Carlo simulations to test variations in campaign strategy (e.g., incentives, call frequency).</li>
      <li>Prioritize campaigns predicted to deliver the highest conversion rates./li>
    </ul>
  </section>

  <section>
    <h2>References</h2>
    <div class="reference-list">
      <p>Banu, S. (2023). BANK MARKETING-Term Deposit Prediction Model. Medium.</p>
      <p>Businesswire (2023). MANTL Announces Growth Marketing Solution...</p>
      <p>Few, S. (2015). Signal: Understanding What Matters in a World of Noise.</p>
      <p>Koh, H. C. (2005). Data mining applications for SMEs.</p>
      <p>Pedamkar, P. (2023). Power BI Bubble Chart. EDUCBA.</p>
      <p>Powell, S. G., & Baker, K. R. (2016). Business analytics with spreadsheets.</p>
      <p>Taylor, S. (2024). Positively Skewed Distribution. CFI.</p>
      <p>Yau, N. (2013). Data Points. John Wiley & Sons.</p>
    </div>
  </section>
</body>
</html>


