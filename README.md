In this data analytics project, I developed AnemiaOptiCare, a comprehensive algorithmic approach for optimizing resource allocation and creating predictive models for maternal anemia management. I utilized a dataset containing prevalence rates of anemia among pregnant women across various countries and years to implement several algorithms addressing key public health optimization challenges. The dataset can be found in the link "https://ourworldindata.org/micronutrient-deficiency". 

### Project Overview and Objectives
My primary goal was to leverage algorithmic techniques to solve resource allocation problems in maternal health, specifically targeting anemia in pregnant women. I focused on developing efficient algorithms for supplement distribution within budget constraints, risk factor identification, policy effectiveness analysis, and prevalence prediction. The project demonstrates how computational approaches can optimize healthcare resource utilization and improve maternal health outcomes.

### Algorithm Implementation and Analysis
# Knapsack Optimization for Supplement Selection
I implemented a dynamic programming approach to solve the 0/1 knapsack problem for supplement allocation. Using effectiveness values derived from anemia prevalence data and costs based on temporal distance from the year 2000, I achieved an optimal effectiveness of 255 within a budget constraint of 100. This algorithm enables healthcare providers to maximize the impact of limited resources by selecting the most effective combination of supplements.

# Bitwise Count Optimization for Risk Factor Analysis
I applied a bitwise count optimization technique to analyze years with multiple risk factors for anemia. By representing risk factors as bits in a binary representation of each year, I identified 4080 years having at least 3 risk factors. This efficient bit manipulation approach provides a computationally optimized method for risk stratification across large temporal datasets.

# Threshold-Based Analysis for At-Risk Population Identification
Using the median prevalence as a threshold, I developed an algorithm to count women at risk of anemia. The analysis identified 2047 instances where anemia prevalence exceeded this threshold. This approach allows for targeted intervention strategies by quantifying the scope of the at-risk population.

# Longest Common Subsequence Analysis for Policy Effectiveness
I implemented a dynamic programming algorithm to find the Longest Common Subsequence between two time-series reports representing years when different anemia reduction policies were effective. The analysis revealed a sequence length of 10, indicating substantial overlap in effective periods between the two policies. This insight helps in identifying time periods when combined policy approaches were particularly successful1.

# Fourier Transform for Cyclical Pattern Detection
By applying Fourier Transform analysis to the time-series data of anemia prevalence, I successfully detected cyclical patterns in the prevalence rates. This finding is crucial for understanding seasonal or periodic fluctuations in anemia rates, which can inform the timing of intervention programs.

# LSTM Neural Network for Prevalence Prediction
I developed and trained a Long Short-Term Memory (LSTM) neural network model to predict future anemia prevalence rates. Using a window size of 3 years, the model predicted a prevalence rate of 32.22% for the upcoming year. This predictive capability enables proactive resource planning and intervention scheduling.

### Visualization: 

# Knapsack Dynamic Programming Heatmap
I created a sophisticated heatmap visualization of the Knapsack Dynamic Programming table using Seaborn's heatmap functionality with a "YlGnBu" color mapping. This visualization transformed the abstract numerical optimization process into an intuitive visual representation where color intensity corresponded to effectiveness values. The heatmap clearly illustrated how the optimal solution (255 effectiveness units) was progressively built through the dynamic programming approach as more countries were considered within the 50-year budget constraint. Specifically, the horizontal axis represented the cumulative years while the vertical axis represented the incremental inclusion of countries, with color gradient indicating total prevalence values at each decision point. This visualization was instrumental in demonstrating how marginal contributions to effectiveness changed as the algorithm approached the budget limit.

# Time-Series Analysis of Global Prevalence Trends
I developed detailed time-series plots tracking anemia prevalence among pregnant women worldwide over multiple years. Using Matplotlib, I filtered the dataset for 'World' entries and plotted prevalence percentages against time with blue markers connected by trend lines. This visualization revealed subtle but important long-term patterns in global anemia rates that would be difficult to detect in tabular data. I enhanced the interpretability by including grid lines and comprehensive axis labels, allowing for precise tracking of year-to-year prevalence changes. The visualization clearly demonstrated periods of decline and stabilization in global anemia rates, providing context for intervention effectiveness assessment.

# Risk Factor Distribution Histograms
I implemented an innovative approach to risk factor analysis using bit manipulation techniques. For each prevalence value, I computed a risk factor count by converting the scaled prevalence (multiplied by 10) to a binary representation and counting the number of '1' bits. This computation was visualized through a purple-colored histogram using Seaborn's histplot function with carefully calibrated bin sizes matching the range of calculated risk factors. The resulting distribution visualization revealed clustering patterns in risk factor counts, with certain count values occurring significantly more frequently than others. This provided critical insights into the natural stratification of risk levels across the global population and identified potential threshold values for intervention targeting.

# LCS Dynamic Programming Matrix Visualization
To analyze policy effectiveness overlap, I developed a detailed heatmap visualization of the Longest Common Subsequence dynamic programming matrix. Using annotation-enabled heatmaps with a "Blues" color scheme, I visually represented the incremental building of common subsequences between two different policy implementation timelines. Each cell in the matrix was labeled with its numerical value, creating a comprehensive map of sequence matching that clearly illustrated where and how the two policies aligned over time. The visualization revealed a maximum sequence length of 10, indicating substantial temporal overlap in effective periods between the two anemia reduction strategies. This visual approach made the abstract concept of sequence alignment immediately accessible to policy planners.
