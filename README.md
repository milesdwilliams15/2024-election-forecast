# 2024 Presidential Election Forecast

For fun, I wanted to try my hand at a 2024 US Presidential election forecast. Here's the current predictions as of 9-29-2024.

[**Note**: *The forecast doesn't currently factor in the separate electoral districts in Maine and Nebraska. In future versions of this, I plan to fix this as it may tilt the range of possible election outcomes more in favor of Donald Trump.*]

First up are state-level predictions for Kamala Harris' popular vote margin relative to Donald Trump's. These predictions are based on a mixed-effects linear model fit using previous election state-level margins for the Democratic Party (going back to 2000) with random intercepts and slopes by state. The results show that Harris is predicted to win nearly all swing states, but by very narrow margins.

![](_figs/predicted_margin_by_st.png)

Second up are state-level likelihoods that Harris will win the popular vote instead of Trump. These likelihoods are based on bootstrapped predictions from the previous model. The results show that Harris is likely to win 4 out of 7 swing states. The model seems certain that she'll win Wisconsin, Michigan, Pennsylvania, and Nevada, but it indicates she'll more than likely lose Arizona, Georgia, and North Carolina.

![](_figs/predicted_win_by_st.png)

Finally, the below figure simulates (based on the previously shown likelihoods) the range of possible Electoral College vote totals Harris is likely to win. The distribution is produced via 10,000 simulations of state-level wins and losses based on predicted probabilities of victory. Harris is predicted to win the 2024 election with a very narrow margin of victory---279 Electoral College votes. This is only 9 more than the 270 she would need to secure the presidency. While there is a lot of uncertainty about this result, the range of empirically supported alternatives is heavily skewed toward a Harris win. Less than a percentage of the simulations are consistent with a tie in the Electoral College, and in no scenario does Trump secure the presidency.

![](_figs/hist_of_wins.png)

## Replication Materials

The code to replicate these results is in the Quarto file `_analysis.qmd`.
