# Experiment Design
## Metric Choice

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

| Metric | Standard Deviation |
|--------|--------------------|
| Gross conversion | 0.0202 |
| Net conversion | 0.0156 |

Both evaluation metrics have the same unit of analysis (user-ids) and unit of diversion (cookies). We can expect the analytical and empirical standard deviation to be similar as user-ids and unique cookies should be very similar. Hoever, it does exist the possibility that a user would login under a different browser or click the "Start free trial" button in two different days. To ensure accuracy it would be recommendable to test the standard deviation.

## Sizing
### Number of Samples vs. Power

The Bonferroni collection will not be used during the analysis phase.

**Test Parameters**
alpha = 0.05
beta = 0.2
power = 0.8


| Metric | Minimum effect size | Baseline Conversion | Sample Size (per group) | Pageviews |
|--------|---------------------|---------------------|-------------------------|-----------|
| Gross conversion | 0.01      |    0.20625          |  25,835                 | 645,875   |
| Net conversion |   0.0075    | 0.1093125           |  27,413                 | 685,325   |

Pageviews required = 685,325

### Duration vs. Exposure
For this experiment we can divert 50% of the traffic. This will allow us to obtain results in a reasonable time while not exposign the entirety of the traffic to the experiment and possible errors or unexpected behaviours clients might have.

Overall, this experiment presents a Low level of risk for Udacity. Identified risks have been outlined below:

Likelihood and impact measured from 1 (lowest) to 5 (highest)

| Risk | Likelihood | Impact | Risk Level     |
|------|------------|--------|----------------|
| New screen does not load | 1 | 3 | Low |
| Faulty experimental setup impedes users from registering | 1 | 5 | Medium |
| Evaluation metrics not properly captured | 2 | 3 | Low |

Fraction of traffic diverted = 0.5
Days needed to run the experiment = 35

# Experiment Analysis
## Sanity Checks

| Metric | Lower Bound | Upper Bound | Observed | Passes |
|--------|-------------|-------------|----------|--------|
| Number of cookies | 0.4988 | 0.5011 | 0.5006 | True |
| Number of clicks on "Start free trial" | 0.4959 | 0.5041 | 0.5005 | True |

## Result Analysis
### Effect Size Tests

| Metric | Lower Bound | Upper Bound | Statistically Significant | Practically Significant |
|--------|-------------|-------------|----------|--------|
| Gross conversion | -0.0291 | -0.0119 | True  | True |
| Net conversion | -0.0116 | 0.0019 | True | False |


### Sign Tests
For each of your evaluation metrics, do a sign test using the day-by-day data, and report the p-value of the sign test and whether the result is statistically significant. (These should be the answers from the "Sign Tests" quiz.)

### Summary
State whether you used the Bonferroni correction, and explain why or why not. If there are any discrepancies between the effect size hypothesis tests and the sign tests, describe the discrepancy and why you think it arose.

## Recommendation
Make a recommendation and briefly describe your reasoning.

# Follow-Up Experiment
Give a high-level description of the follow up experiment you would run, what your hypothesis would be, what metrics you would want to measure, what your unit of diversion would be, and your reasoning for these choices.
