# Tactical-Analysis-of-Back-line-formations-in-Soccer
This repository contains the analysis of defensive line structures in professional women’s football, focusing on the NWSL and WSL. The project quantifies offensive threat (xThreat) and evaluates how formations like the Back 3, 4, and 5 influence performance across different phases of play.
# Project Overview
The objective of this study is to understand how defensive shapes affect vulnerability across channels and game phases, and how these patterns vary based on team strength and league.
# Dataset
The analysis utilizes 213 professional matches featuring:
* Event & Tracking data
* Possession sequences
* Passing options and off-ball runs

Note: The data was filtered to frames where teams were out of possession in their defensive third to accurately assess backline performance.

# Methodology: Automated Detection
Since 75% of data frames lacked explicit defensive labels, we implemented an automated detection system. Four approaches were tested:
* Linear Regression: Fits a line to the deepest defenders.
* DBSCAN: Density-based clustering; robust to outliers.
* Optimal Thresholding: Searches for the X-position creating the tightest defender group.
* K-Means Clustering (Selected): Clusters defenders by depth after removing the goalkeeper. This was chosen for its consistency and robustness to formation changes.

# Key Insights
## Formation Trends
* Predominant Shape: Teams consistently spend the longest duration in a Back 4.
* Effectiveness: xThreat generally decreases as the number of defenders in the back line increases.
* League Differences: WSL teams utilize a Back 5 more frequently when facing Top-4 opponents (reactive approach), while NWSL teams maintain a steadier reliance on the Back 4.

## Performance & Vulnerabilities
* Transition Weakness: Top-4 teams are particularly vulnerable in a Back 3 during quick breaks, transitions, and direct phases. This is often due to full-backs advancing high, leaving space behind for counter-attacks.
* Channel Vulnerability: Top teams concede a high ratio of dangerous passes from wide and half-space channels into the central zone when defending with a Back 3 or 4.
* Pass Completion: Pass completion probability consistently decreases as the ball moves from wide channels to the central channel, regardless of the formation used.

## Team-Specific Analysis
### Bristol City Women
High xThreat conceded when out of their Back 5 justified their mid-season switch to that formation.
### Leicester City Women
The only team to concede a higher xThreat in a Back 4 than a Back 3.
### Manchester United Women
High vulnerability in a Back 3 during transitions due to aggressive full-back advancement.
### Everton Women
Used defensive midfielder C. Wheeler as a wingback, which sometimes affected defensive balance in wide channels.
### Houston Dash
Successfully utilized a shifting Back 3 to 5 to concede the second-fewest goals in the league.

# Future Work
* Interactive Dashboard: Build a tool to explore xThreat patterns and phase-specific vulnerabilities.
* Offensive Behavior: Examine how these defensive shapes influence ball progression and chance creation.
* Impact Modeling: Quantify how individual players (CBs, FBs) affect xThreat conceded within each formation.
* Decision-Making: Model when wing-backs should drop into a Back 5 versus remaining high to support possession.
