# Experiment Design
## Metric Choice
List which metrics you will use as invariant metrics and evaluation metrics here. (These should be the same metrics you chose in the "Choosing Invariant Metrics" and "Choosing Evaluation Metrics" quizzes.)
For each metric, explain both why you did or did not use it as an invariant metric and why you did or did not use it as an evaluation metric. Also, state what results you will look for in your evaluation metrics in order to launch the experiment.

| Metric | Metric Type | Comments |
|--------|-------------|----------|
| Number of cookies | Invariant | The number of cookies to view the source page will not be affected by the experiment as the experiment happens after the page loads. |
| Number of clicks | Invariant | This is the event that will trigger the new screen, the same amount of cookies should appear in the control and experiment groups. |
| Gross conversion | Evaluation | This metric will provide a good estimation of the effect of the new screen. If the experiment is successful, the gross conversion will be lower in the experiment than in the control group as it will eliminate students that do not have the necessary time availability. |
| Net conversion | Evaluation | This metric will provide a good estimation of the effect of the new screen. If the experiment is successful, the net conversion will increase as more students with the necessary time availability will remain in the course out of the total number of cookies that trigger the experiment. |
| Number of user-ids | N/A | This metric was not used as will be affected by the experiment (not invariant) yet does not provide a good comparison between the control and experiment groups for the experiment. |
| Click-through probability | N/A | This metric could have been used as an invariant metric as it is not affected by the experiment; however, having two invariant metrics was sufficient. |
| Retention | N/A | This metric could have been used as an evaluation metric; hoever, the amount of observations required to make the experiment powerfull enough would have taken too long to collect and was not practical. |

## Measuring Standard Deviation
List the standard deviation of each of your evaluation metrics. (These should be the answers from the "Calculating standard deviation" quiz.)

For each of your evaluation metrics, indicate whether you think the analytic estimate would be comparable to the the empirical variability, or whether you expect them to be different (in which case it might be worth doing an empirical estimate if there is time). Briefly give your reasoning in each case.

## Sizing
### Number of Samples vs. Power
Indicate whether you will use the Bonferroni correction during your analysis phase, and give the number of pageviews you will need to power you experiment appropriately. (These should be the answers from the "Calculating Number of Pageviews" quiz.)

### Duration vs. Exposure
Indicate what fraction of traffic you would divert to this experiment and, given this, how many days you would need to run the experiment. (These should be the answers from the "Choosing Duration and Exposure" quiz.)

Give your reasoning for the fraction you chose to divert. How risky do you think this experiment would be for Udacity?

# Experiment Analysis
## Sanity Checks
For each of your invariant metrics, give the 95% confidence interval for the value you expect to observe, the actual observed value, and whether the metric passes your sanity check. (These should be the answers from the "Sanity Checks" quiz.)

For any sanity check that did not pass, explain your best guess as to what went wrong based on the day-by-day data. Do not proceed to the rest of the analysis unless all sanity checks pass.

## Result Analysis
### Effect Size Tests
For each of your evaluation metrics, give a 95% confidence interval around the difference between the experiment and control groups. Indicate whether each metric is statistically and practically significant. (These should be the answers from the "Effect Size Tests" quiz.)

### Sign Tests
For each of your evaluation metrics, do a sign test using the day-by-day data, and report the p-value of the sign test and whether the result is statistically significant. (These should be the answers from the "Sign Tests" quiz.)

### Summary
State whether you used the Bonferroni correction, and explain why or why not. If there are any discrepancies between the effect size hypothesis tests and the sign tests, describe the discrepancy and why you think it arose.

## Recommendation
Make a recommendation and briefly describe your reasoning.

# Follow-Up Experiment
Give a high-level description of the follow up experiment you would run, what your hypothesis would be, what metrics you would want to measure, what your unit of diversion would be, and your reasoning for these choices.
