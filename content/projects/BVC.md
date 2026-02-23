+++
date = '2025-03-21T21:55:02-06:00'
draft = false
title = 'Venture Capital 3.0: Riding the ChatGPT Wave'
+++

*March 2025 - May 2025*

### Background

In my Senior Year at Notre Dame, we were tasked to complete a group project utilizing concepts we used from our Urban Analytics class. This project centered around examining key factors that contribute to successful AI investments from both the startup and investor perspectives. By analyzing the generative AI (Gen AI) effect, U.S. government funding, and co-investor networks, this study aimed to uncover how the recent Gen AI trend and VC connectivity impact startups’ visibility in attracting funds and investors’ next-step strategies.

### My roles in this project
- Analyzing general background on how Chat GPT’s founding impacted the business landscape of venture capital 
- Exploratory data analysis (EDA) on all three datasets that were utilized
- Focusing on detailed analysis on the AI Deals Dataset
- Executive summary and conclusion sections of the report 

### What we did
Our team of three conducted a multi-layered analysis of AI startup funding from 2016–2025 to understand how the rise of generative AI reshaped venture capital behavior. We approached the project from three complementary angles: startup performance, government participation, and investor network structure.

1. Measured the “Gen AI Effect” on Startup Success

We classified AI startups into Gen AI and Non-Gen AI categories using keyword tagging and homepage filtering. After cleaning and restructuring the dataset, we:
- Compared funding outcomes (total capital raised, first financing size, time to first financing)
- Examined growth rates and top 10% funding performance
- Built a logistic regression model to identify statistically significant predictors of startup success

We found that Gen AI startups were more likely to reach above-average funding levels and break into the top 10% of total capital raised. They also raised capital faster and in larger initial rounds.


![genAI vs non genAI](1.png)
![genAI vs non genAI](2.png)
![logistic regression](3.png)

2. Analyzed U.S. Government Participation in AI Funding

We explored the role of government-backed investments by filtering deals involving U.S. agencies. Because financial variables were incomplete in this subset, we pivoted toward geospatial and categorical analysis.

We discovered:
- Government AI investments were primarily structured as grants
- Funding was heavily concentrated in the Northeast (New York and Massachusetts)
- Government agencies initially played central roles in early AI funding ecosystems

This revealed how policy shifts in grant allocation could meaningfully affect regional AI development.

![deal types](4.png)
![map of deals](5.png)

3. Conducted Venture Capital Network Analysis (My Primary Contribution)

For the AI deals dataset, I led the exploratory data analysis and built the co-investor network framework.

We:
- Filtered AI deals post-2016 with ≥ $5M investment and ≥ 3 investors
- Constructed rolling 5-year co-investor networks
- Calculated centrality metrics (degree, betweenness, closeness, eigenvector)
- Tracked how investor influence evolved over time

The results showed increasing interconnectedness among AI investors. While government agencies initially held influential network positions, private accelerators — especially Y Combinator — became dominant in both connectivity and influence in recent years. This demonstrated a shift from public-sector-driven AI funding toward a more centralized, private-sector-led ecosystem.

![VC network effect](6.png)
![VC network effect](7.png)
![VC network effect](8.png)
![VC network effect](9.png)
![VC network effect](10.png)

4. Created a visual dashboard using the Shiny App program through R Programming

This dashboard allows users to input:
- Whether or not their startup is generative AI
- Number of active investors
- Number of former investors
- First Financing Size (USD Mn)
- Most Recent Financing Size (USD Mn)
- Growth Rate Change (%)
- Years to First Financing

After the user inputs these fields the dashboard, The Predicted Probability of Top 10% Funding graph shows how a startup’s likelihood of reaching the top 10% of total funding changes as its growth rate shifts, while all other characteristics are held constant. If the curve slopes upward, it indicates that higher growth rates are associated with a greater probability of reaching elite funding levels. A steeper slope suggests that growth rate is a strong predictor in the model, while a flatter line would indicate weaker influence. This visualization essentially performs a sensitivity analysis, illustrating how much projected funding success responds to changes in growth performance.

Additionally, a model summary plot will provide the statistical foundation behind those predictions. It displays the estimated coefficients for each variable in the logistic regression, along with their standard errors, z-values, and p-values. The sign of each coefficient (positive or negative) indicates whether that variable increases or decreases the likelihood of being in the top 10% of funded startups, while statistical significance levels indicate whether the effect is likely meaningful rather than due to chance. The summary also includes model fit statistics such as residual deviance and AIC, which help evaluate how well the model explains the data.
![Shiny App](11.png)

### Conclusion

Our findings suggest that the release of ChatGPT acted as a market shock that accelerated capital concentration around generative AI startups and strengthened network centralization among key private investors.

Three key insights emerged:
1. Gen AI startups have a measurable funding advantage, particularly in reaching the top 10% of total capital raised.
2. Government funding is geographically concentrated and primarily grant-based, making it vulnerable to policy shifts.
3. Investor networks are becoming denser and more centralized, with highly connected investors playing an outsized role in shaping funding trajectories.

For founders, this means network positioning and alignment with Gen AI trends significantly influence funding success. For investors, co-investor centrality and strategic positioning within funding networks matter more than raw deal count alone.

### HTML Report 
[VC HTML Report](/portfolio/VCreport.html)