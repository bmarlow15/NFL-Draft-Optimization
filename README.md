# NFL Draft Optimization Model

## Business Problem

Every year, NFL teams face the high-stakes challenge of optimizing their draft selections to build a competitive roster. The process involves weighing positional needs, available draft capital, and the inherent risk of each pick.  This project aims to create a data-driven framework to identify undervalued draft slots, enabling a team to make more strategic decisions during the NFL Draft. The goal is to move beyond traditional scouting and gut feelings and instead use a quantitative approach to find inefficiencies in the draft market.

## Data Sources

The analysis is based on historical NFL draft data. Each of the 256 draft picks is assigned a value based on various established models, including the Jimmy Johnson, Rich Hill, and Fitzgerald-Spielberger charts. The dataset was limited to the first 222 picks to exclude the less significant later rounds and focused on a subset of 8 teams for a more manageable analysis. 

## Methodology

The core of this project is a least absolute deviations (LAD) regression model built in Python using the Pyomo library.  The model was designed to estimate the "true" value of a draft pick based on the historical data. The steps included:

1.  **Data Collection and Cleaning:** Gathered historical draft pick data and cleaned it to prepare for analysis.
2.  **Feature Engineering:** Utilized established draft value charts (Jimmy Johnson, Rich Hill, etc.) as features in the model.
3.  **Model Building:** Developed a LAD regression model to predict the expected draft position given the chart values.
4.  **Analysis and Validation:** Analyzed the model's output to identify undervalued and overvalued picks for specific teams, such as the Dallas Cowboys and Kansas City Chiefs. The model's accuracy was validated through residual analysis and out-of-sample testing. 

## Results and Insights

The analysis revealed that it's possible to quantify the value of draft picks and identify teams that are more adept at capitalizing on their draft assets.  Key insights include:

* **Valuation as a Strategic Tool:** The model provides a guide for teams to use when considering trades, helping them to assess whether to keep or trade their picks. 
* **Case Study: Kansas City Chiefs:** The model indicated that the Chiefs' successful 2022 draft was, in part, due to the high value of their picks in the early to middle rounds.  This suggests that the team's front office made strategic decisions that aligned with the model's findings.

This project demonstrates that a quantitative approach can provide a significant edge in the high-stakes environment of the NFL Draft.
