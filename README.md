# Strikeout Differential vs Run Differential: Which Predicts Team Win Percentage Best ⚾

Recently, I was listening to the Blair & Barker podcast (Blue Jays podcast), and they had a guest from the Colorado Rockies analyst team. He said something interesting that sparked this quick project. He said 'Strikeout Differential signals a better team than run differential... The [Blue Jays] pitching staff has struck out more than their offense has, and it's by 300.' That is the first time I've ever heard use strikeout differential as a strong predictor for team wins. 

# SetUp/Methodology ⚾

Utilized the **pybaseball** package in Python to access MLB team batting and pitching statistics over the last 20 years (excluded the shortened 2020 season to avoid anomalies).

Scraped team-level metrics including:

Batting stats: Team strikeout rate (K%), runs scored (R), and total strikeouts (SO).

Pitching stats: Wins (W), losses (L), runs allowed (RA), and strikeouts by pitchers (SO_P).

Combined these datasets to calculate run differential (Run_Diff) as the difference between runs scored and runs allowed, and strikeout differential (Strikeout_Diff) as the difference between pitcher strikeouts and batter strikeouts.

**Libraries:**

**pybaseball**: For scraping MLB data.

**pandas & numpy**: For data manipulation.

**matplotlib & seaborn**: For visualizations.

**scikit-learn**: For regression analysis.




