# Strikeout Differential vs Run Differential: Which Predicts Team Win Percentage Best ⚾

Recently, I was listening to the Blair & Barker podcast (Blue Jays podcast), and they had a guest from the Colorado Rockies analyst team. He said something interesting that sparked this quick project. He said 'Strikeout Differential signals a better team than run differential... The [Blue Jays] pitching staff has struck out more than their offense has, and it's by 300.' That is the first time I've ever heard use strikeout differential as a strong predictor for team wins. 

# SetUp/Methodology 

Utilized the **pybaseball** package in Python to access MLB team batting and pitching statistics over the last 20 years (excluded the shortened 2020 season to avoid anomalies).

Scraped team-level metrics including:

Batting stats: Team strikeout rate (K%), runs scored (R), and total strikeouts (SO).

Pitching stats: Wins (W), losses (L), runs allowed (RA), and strikeouts by pitchers (SO_P).

Combined these datasets to calculate run differential (Run_Diff) as the difference between runs scored and runs allowed, and strikeout differential (Strikeout_Diff) as the difference between pitcher strikeouts and batter strikeouts.

# Libraries

**pybaseball**: For scraping MLB data.

**pandas & numpy**: For data manipulation.

**matplotlib & seaborn**: For visualizations.

**scikit-learn**: For regression analysis.


# Analysis

<img width="846" height="468" alt="image" src="https://github.com/user-attachments/assets/8be3e3ba-ae1d-4063-a2c8-039628da0fe2" />

First of all, the figure above displays the relationship between Run Differential and Win Percentage. A $R^2$ of 0.88 shows that run differential is a strong predictor for win percentage, aligning with traditional baseball analytics.

<img width="846" height="468" alt="image" src="https://github.com/user-attachments/assets/14df2c1f-8058-4ea5-bab4-fb81cff16d4b" />
<img width="846" height="468" alt="image" src="https://github.com/user-attachments/assets/d0df4d9b-9af8-4396-a9d4-6e1923033d49" />

Before getting into strikeout differential, I looked at the team's batting strikeout rate relationship with Win Percentage. The low $R^2$ shows there are little to no relationships between the variables and even after 2020, where strikeout rates are more prominent due to the chase for more power/home runs, there are no relationships.


<img width="846" height="468" alt="image" src="https://github.com/user-attachments/assets/5dc16c35-2f9b-4353-91c6-72fc24e068a4" />
<img width="846" height="468" alt="image" src="https://github.com/user-attachments/assets/5bddac5c-e704-4bc5-8198-d887e99c2043" />

Looking at the strikeout differential now, there is a moderately positive correlation with the Win Percentage, with a higher level of correlation post-2020. The analysis supports the modern baseball emphasis on strikeout-heavy pitching, as it correlates with winning. However, the modest R^2 suggests teams should balance this with other metrics like walk rates, defensive skills, or clutch hitting to optimize performance. 

# Conclusion

In conclusion, while the strikeout differential does have a moderate positive correlation with Wins, run differential remains the best predictor for Wins. Run differential accounts for all aspects of the game: offense (hitting, baserunning), pitching (run prevention), and defense (fielding errors, defensive plays). This makes it a holistic measure of team performance. Strikeout differential excludes Walks, home runs, defensive errors, baserunning, and situational hitting (e.g., clutch hitting with runners in scoring position). In the end, the guy in that podcast was wrong.








