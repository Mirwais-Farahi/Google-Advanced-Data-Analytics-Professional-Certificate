# Two-Sample Hypothesis Test for Comparing Means

## Overview

In recent discussions, we explored how professionals use the two-sample hypothesis test to determine whether the difference between two sample means is statistically significant or merely due to chance. This test is particularly useful for A/B tests, which compare how two groups of users respond to different versions of a product or website. For example, an A/B test can help determine if observed differences in average click rates are attributable to changes in website design or random variation.

## Scenario

In this example, you're working as a data professional for the Department of Education of a large nation. You are analyzing data on literacy rates across districts. Specifically, you're tasked with comparing the mean district literacy rates for two states, State 21 and State 28. State 28 has almost 40 districts, and State 21 has more than 70. Due to time and resource constraints, you survey 20 randomly chosen districts from each state.

Your goal is to determine if the observed difference in literacy rates between the two states is statistically significant. This analysis will guide the distribution of government funding to improve literacy.

## Steps for Conducting a Two-Sample T-Test

1. **State Hypotheses**:
    - **Null Hypothesis (H0)**: There is no difference in the mean district literacy rates between State 21 and State 28.
    - **Alternative Hypothesis (H1)**: There is a difference in the mean district literacy rates between State 21 and State 28.

2. **Choose a Significance Level**:
    - Set the significance level (alpha) to 0.05 (5%).

3. **Compute the P-Value**:
    - The p-value represents the probability of observing a difference as extreme as, or more extreme than, the observed difference if the null hypothesis is true.

4. **Reject or Fail to Reject the Null Hypothesis**:
    - If the p-value is less than the significance level, reject the null hypothesis.
    - If the p-value is greater than the significance level, fail to reject the null hypothesis.

## Python Implementation

1. **Import Necessary Libraries**:
    ```python
    import pandas as pd
    from scipy import stats
    ```

2. **Filter Data for States**:
    ```python
    state_21 = df[df['state_name'] == 'State 21']
    state_28 = df[df['state_name'] == 'State 28']
    ```

3. **Random Sampling**:
    ```python
    sampled_state_21 = state_21.sample(n=20, replace=True, random_state=13490)
    sampled_state_28 = state_28.sample(n=20, replace=True, random_state=39103)
    ```

4. **Calculate Mean Literacy Rates**:
    ```python
    mean_state_21 = sampled_state_21['literacy_rate'].mean()
    mean_state_28 = sampled_state_28['literacy_rate'].mean()
    ```

5. **Perform Two-Sample T-Test**:
    ```python
    t_stat, p_value = stats.ttest_ind(sampled_state_21['literacy_rate'], sampled_state_28['literacy_rate'], equal_var=False)
    ```

6. **Interpreting Results**:
    - **P-Value**: Approximately 0.0064 (0.64%).
    - Since the p-value is less than 0.05, reject the null hypothesis. There is a statistically significant difference between the mean literacy rates of State 21 and State 28.

## Conclusion

The two-sample t-test results indicate a statistically significant difference between the literacy rates of the two states. The state with the lower literacy rate (State 28) will likely receive more resources to improve literacy. This method is a powerful tool for data professionals to make data-driven decisions and help stakeholders allocate resources effectively.

# Python scipy ttest_ind
## Alternative Hypothesis in `stats.ttest_ind`

The `alternative` parameter in the `stats.ttest_ind` function is used to specify the type of alternative hypothesis you want to test. By default, the t-test is a two-tailed test, which checks for any difference between the two sample means. However, you can specify a one-tailed test by setting the `alternative` parameter.

### Options for `alternative` Parameter:

- **`alternative='less'`**: 
    - This performs a one-tailed test where the alternative hypothesis is that the mean of the first sample is less than the mean of the second sample.
    - **Hypotheses**:
        - \( H_0: \mu_{\text{first}} \geq \mu_{\text{second}} \)
        - \( H_1: \mu_{\text{first}} < \mu_{\text{second}} \)

- **`alternative='greater'`**:
    - This performs a one-tailed test where the alternative hypothesis is that the mean of the first sample is greater than the mean of the second sample.
    - **Hypotheses**:
        - \( H_0: \mu_{\text{first}} \leq \mu_{\text{second}} \)
        - \( H_1: \mu_{\text{first}} > \mu_{\text{second}} \)

- **`alternative='two-sided'`** (default):
    - This performs the standard two-tailed test, where the alternative hypothesis is that the two means are different.
    - **Hypotheses**:
        - \( H_0: \mu_{\text{first}} = \mu_{\text{second}} \)
        - \( H_1: \mu_{\text{first}} \neq \mu_{\text{second}} \)

Use these options to tailor your t-test to the specific hypothesis you are testing.
