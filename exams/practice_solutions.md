# Statistics for Business Administration — Detailed Solutions

---

## TOPIC 1: Study Design, Sampling & Descriptive Statistics

### Solution 1.1

**a)** This is an **observational study** — the researchers merely observe and record coffee consumption and heart rate without assigning or manipulating any variables.

**No**, the results **cannot** be used to establish a causal relationship. Observational studies can only show associations/correlations, not causation. There may be confounding variables (e.g., stress, age, physical activity) that affect both coffee consumption and heart rate. Only randomized experiments with random assignment to treatment groups can establish causality.

**b)** This is **non-response bias** (also acceptable: voluntary response bias). People who choose to respond may differ systematically from those who do not — for example, those with health concerns may be more motivated to respond, leading to a non-representative sample.

---

### Solution 1.2

**a)** This is an **observational study** using a **stratified sample**. The five faculties serve as strata, and a random sample is drawn from each stratum. This ensures representation from all faculties.

**b)** This is a **cluster sample**. The lecture halls are the clusters, and all individuals within the selected clusters are surveyed. The key difference: in stratified sampling, you sample *within* each group; in cluster sampling, you select entire groups.

---

### Solution 1.3

**a)** The new median is still **€52,000**.

The median is the value such that at least half the observations are ≤ the median and at least half are ≥ the median. The CEO's salary was already the maximum value. Changing it from €890,000 to €950,000 only affects the very top of the distribution — it does not change the position of any value around the middle. Since n = 200, the median is determined by the 100th and 101st ordered values, which are unaffected.

**b)** The mean will **increase**. The mean is sensitive to every value in the dataset. Increasing one value by €60,000 increases the sum, and therefore:

New mean = Old mean + (950,000 − 890,000)/200 = Old mean + 300

So the mean increases by €300.

---

### Solution 1.4

- **P₁**: Valid. Sum = 0.25 + 0.25 + 0.25 + 0.25 = 1.0, and all probabilities are between 0 and 1. ✓
- **P₂**: **Invalid**. Sum = 0.30 + 0.25 + 0.35 + 0.15 = **1.05 > 1**. The probabilities must sum to exactly 1.
- **P₃**: **Invalid**. Sum = 0.10 + 0.20 + 0.30 + 0.50 = **1.10 > 1**. Again, the probabilities exceed 1 in total.

---

## TOPIC 2: Probability & Bayes' Theorem

### Solution 2.1

**a)** Let D = "component is defective." Using the law of total probability:

P(D) = P(D|A)·P(A) + P(D|B)·P(B) + P(D|C)·P(C)

P(D) = 0.02 × 0.50 + 0.03 × 0.30 + 0.05 × 0.20

P(D) = 0.010 + 0.009 + 0.010 = **0.029**

So there is a 2.9% chance a randomly selected component is defective.

**b)** Using Bayes' Theorem:

P(C|D) = P(D|C) · P(C) / P(D)

P(C|D) = (0.05 × 0.20) / 0.029

P(C|D) = 0.010 / 0.029 = **0.3448 ≈ 34.5%**

Despite producing only 20% of components, Machine C is responsible for about 34.5% of defective ones, reflecting its higher defect rate.

---

### Solution 2.2

Let P = "passed" and T = "attended tutorials regularly."

Given:
- P(P) = 0.65, P(P^c) = 0.35
- P(T|P) = 0.80
- P(T|P^c) = 0.30

We want P(P|T). By Bayes' Theorem:

P(P|T) = P(T|P) · P(P) / [P(T|P) · P(P) + P(T|P^c) · P(P^c)]

P(P|T) = (0.80 × 0.65) / (0.80 × 0.65 + 0.30 × 0.35)

P(P|T) = 0.52 / (0.52 + 0.105) = 0.52 / 0.625 = **0.832**

A student who attended tutorials regularly has an 83.2% probability of having passed.

---

### Solution 2.3

**a)** To check independence, we compare conditional probabilities across age groups:

P(Brand X | 18-30) = 45/80 = 0.5625
P(Brand X | 31-50) = 30/70 = 0.4286
P(Brand X | 51+) = 15/50 = 0.3000

Since these probabilities **differ** across age groups, brand preference is **not independent** of age group. If they were independent, P(Brand X | age group) would be the same for all groups (and equal to the marginal P(Brand X) = 90/200 = 0.45).

**b)** P(Brand X | 18-30) = 45/80 = **0.5625**

---

### Solution 2.4

**a)** Using the addition rule:

P(A ∪ B) = P(A) + P(B) − P(A ∩ B)

0.7 = 0.4 + 0.5 − P(A ∩ B)

P(A ∩ B) = 0.9 − 0.7 = **0.2**

**b)** For independence, we need P(A ∩ B) = P(A) · P(B).

P(A) · P(B) = 0.4 × 0.5 = 0.2

Since P(A ∩ B) = 0.2 = P(A) · P(B), the events A and B **are independent**. ✓

---

## TOPIC 3: Discrete Probability Distributions

### Solution 3.1

**a)** Let X = number of households owning an electric vehicle. Since we have a fixed number of independent trials (n = 25), each with the same probability of success (p = 0.12):

**X ~ Binomial(n = 25, p = 0.12)**

**b)** P(X = 3) = C(25,3) · 0.12³ · 0.88²²

From the hint: `dbinom(0:5, size = 25, prob = 0.12)` gives probabilities for X = 0, 1, 2, 3, 4, 5.

The 4th value (index 3, since R starts at X=0) is: P(X = 3) = **0.2213**

---

### Solution 3.2

**a)** With λ = 4.5 calls/hour and X ~ Poisson(4.5):

P(X = 6) = e^(-4.5) · 4.5⁶ / 6!

From the hint: `dpois(0:8, lambda = 4.5)`, the 7th value (index 6) is:

P(X = 6) = **0.12814**

**b)** P(X ≤ 2) = P(X = 0) + P(X = 1) + P(X = 2)

From `ppois(0:5, lambda = 4.5)`, the 3rd value (index 2) is:

P(X ≤ 2) = **0.17358**

So there is about a 17.4% chance of receiving at most 2 calls in one hour.

---

### Solution 3.3

**a)** First, identify the probabilities:
- Hearts: 13 cards → win €3
- Face cards that are NOT hearts: 3 face cards × 3 remaining suits = 9 cards → win €7
- All other cards: 52 − 13 − 9 = 30 cards → lose €2

E(X) = 3 · (13/52) + 7 · (9/52) + (−2) · (30/52)

E(X) = 3 · 0.25 + 7 · 0.1731 + (−2) · 0.5769

E(X) = 0.75 + 1.2115 − 1.1538 = **0.8077 ≈ €0.81**

**b)** Over 100 games, expected total winnings = 100 × 0.81 = **€80.77**

---

## TOPIC 4: Normal Distribution & Central Limit Theorem

### Solution 4.1

**a)** Standardize:
- Z₁ = (2.0 − 2.5) / 0.4 = −1.25
- Z₂ = (3.0 − 2.5) / 0.4 = 1.25

P(2.0 < X < 3.0) = P(−1.25 < Z < 1.25) = 1 − 2 · P(Z > 1.25)

From the hint: P(Z > 1.25) = 0.10565

P = 1 − 2 × 0.10565 = 1 − 0.21130 = **0.7887 ≈ 78.9%**

**b)** Z = (3.2 − 2.5) / 0.4 = 1.75

P(X > 3.2) = P(Z > 1.75) = **0.04006 ≈ 4.0%**

---

### Solution 4.2

**a)**
- E(X̄) = μ = **100**
- SD(X̄) = σ/√n = 16/√64 = 16/8 = **2**

**b)** By the CLT, X̄ is approximately normally distributed.

Z = (104 − 100) / 2 = 2

P(X̄ > 104) = P(Z > 2) = **0.02275 ≈ 2.3%**

---

## TOPIC 5: Confidence Intervals

### Solution 5.1

**a)** Conditions for CLT-based inference:
1. **Independence**: The sample is random, so observations can be considered independent. ✓
2. **Sample size**: n = 120 ≥ 30, which is large enough for the CLT to apply even if the population distribution is somewhat skewed. ✓

Both conditions are met.

**b)** The 95% CI is: x̄ ± z* · SE

SE = s/√n = 62/√120 = 62/10.954 = 5.659

z* = z₀.₉₇₅ = 1.96

CI = 285 ± 1.96 × 5.659 = 285 ± 11.09

**CI = (273.91, 296.09)**

**c)** We are 95% confident that the true average monthly food spending of all university students is between €273.91 and €296.09.

*Important: This does NOT mean there is a 95% probability the true mean falls in this interval. The true mean is fixed; the confidence level refers to the method's long-run success rate.*

---

### Solution 5.2

**a)** The confidence interval is centered at the sample mean. The margin of error is half the width:

ME = (34.7 − 28.3) / 2 = 6.4 / 2 = **3.2 minutes**

(Sample mean = 28.3 + 3.2 = 31.5 minutes)

**b)** A 95% confidence interval would be **wider**. A higher confidence level requires a larger critical value (z* increases from 1.645 to 1.96), resulting in a larger margin of error. The interval must be wider to capture the true parameter with higher confidence.

---

### Solution 5.3

SE = √(s₁²/n₁ + s₂²/n₂) = √(3.1²/35 + 3.8²/40)

SE = √(9.61/35 + 14.44/40) = √(0.2746 + 0.3610) = √0.6356 = 0.7972

z* = z₀.₉₇₅ = 1.96

**Margin of Error = 1.96 × 0.7972 = 1.563 days**

The 95% CI for (μ_A − μ_B) would be:
(12.4 − 14.2) ± 1.563 = −1.8 ± 1.563 = **(−3.363, −0.237)**

Since the interval does not contain 0, there is evidence of a significant difference in recovery times.

---

## TOPIC 6: Hypothesis Testing

### Solution 6.1

**a) FALSE.** The null hypothesis is H₀: μ = 50, NOT μ = 47.35. The output states "alternative hypothesis: true mean is not equal to 50", which means H₀: μ = 50. The value 47.35 is the sample mean (the estimate), not the hypothesized value.

**b) FALSE.** The p-value is 0.0783, which is **greater** than α = 0.05. Therefore, we **fail to reject** H₀. Alternatively, 50 is contained within the 95% CI [44.12, 50.58], which also indicates we cannot reject H₀: μ = 50 at the 5% level.

**c) TRUE.** The confidence interval is x̄ ± ME, so:
ME = upper bound − x̄ = 50.58 − 47.35 = 3.23 ✓
(Check: x̄ − ME = 47.35 − 3.23 = 44.12 ✓)

**d) TRUE.** A 90% CI is **narrower** than a 95% CI. Since the 95% CI barely includes 50 (the upper bound is 50.58), a narrower 90% CI would likely exclude 50. Furthermore, the p-value for a two-sided test is 0.0783 < 0.10, which means we would reject H₀ at the 10% significance level, confirming that 50 is NOT in the 90% CI.

---

### Solution 6.2

**a)**
- H₀: μ ≥ 14 (or equivalently μ = 14)
- H_A: μ < 14

This is a one-sided test because the consumer magazine wants to show the battery life is **less than** claimed.

**b)** Test statistic:

T = (x̄ − μ₀) / SE = (13.2 − 14) / (2.4/√36) = −0.8 / 0.4 = **−2.0**

**c)** From the hint: P(T ≤ −2) = pt(-2, df=35) = 0.02680

The p-value for this one-sided test is **0.0268**.

Since 0.0268 < 0.05, we **reject H₀** at the 5% significance level. The data provides convincing evidence that the average battery life is less than 14 hours.

---

### Solution 6.3

**a)** A **paired t-test** is appropriate. The same participants are measured twice (before and after), making the observations paired/dependent. We analyze the differences d_i = before_i − after_i.

**b)**
- H₀: μ_d = 0 (no average weight change)
- H_A: μ_d > 0 (average weight loss, since d = before − after > 0 means loss)

**c)** Test statistic:

T = d̄ / (s_d/√n) = 2.3 / (4.1/√28) = 2.3 / (4.1/5.292) = 2.3 / 0.7746 = **2.969**

Degrees of freedom: df = n − 1 = 27

From the hint: t₀.₉₅(27) = 1.703 and t₀.₉₇₅(27) = 2.052

Since this is one-sided, we compare T = 2.969 with t₀.₉₅(27) = 1.703.

Since 2.969 > 2.052, we know the p-value < 0.025 (< 0.05).

**Conclusion:** We reject H₀ at α = 0.05. The data provides convincing evidence that the diet leads to significant weight loss.

---

### Solution 6.4

**a)**
- H₀: p = 0.33
- H_A: p > 0.33 (one-sided, testing if support is **higher**)

**b)** Test statistic:

SE₀ = √(p₀(1 − p₀)/n) = √(0.33 × 0.67/250) = √(0.2211/250) = √0.0008844 = 0.02974

Z = (p̂ − p₀) / SE₀ = (0.38 − 0.33) / 0.02974 = 0.05 / 0.02974 = **1.681**

**c)** This is one-sided, so p-value = P(Z > 1.681).

From the hint: P(Z > 1.64) = 0.0505

Since 1.681 > 1.64, the p-value < 0.0505. This is very close to 0.05 but just below it.

**Conclusion:** At α = 0.05, we marginally reject H₀. The data provides evidence that the city's support for the initiative is higher than the national average, though the evidence is borderline.

---

## TOPIC 7: Chi-Squared Tests

### Solution 7.1

**a)** H₀: The distribution of preferred social media platforms among teenagers follows the hypothesized distribution (Instagram: 40%, TikTok: 35%, YouTube: 15%, Other: 10%).

**b)** Expected counts = n × p₀:
- Instagram: 300 × 0.40 = **120**
- TikTok: 300 × 0.35 = **105**
- YouTube: 300 × 0.15 = **45**
- Other: 300 × 0.10 = **30**

**c)** Conditions:
1. **Independence**: Sample is random. ✓
2. **Expected counts**: All expected counts must be ≥ 5. The smallest expected count is 30. ✓

Both conditions are satisfied, so the chi-squared test can be used.

---

### Solution 7.2

**a)** H₀: Learning style preference and academic major are independent.

**b)** Both variables have 3 levels, so:

df = (r − 1)(c − 1) = (3 − 1)(3 − 1) = **4**

**c)** From the hint with df = 4:
- qchisq(0.1, df=4, lower.tail=FALSE) = 7.779
- qchisq(0.05, df=4, lower.tail=FALSE) = 9.488

Our test statistic is 8.2.

Since 7.779 < 8.2 < 9.488, we have:

P(χ² > 9.488) = 0.05 < p-value < P(χ² > 7.779) = 0.10

So the **p-value is between 0.05 and 0.10**.

At α = 0.05, since the p-value > 0.05, we **fail to reject H₀**. There is not sufficient evidence at the 5% level to conclude that learning style preference and academic major are dependent.

---

### Solution 7.3

**a)** Expected count = (row total × column total) / table total

E(Exercises regularly, High Stress) = (170 × 90) / 350 = 15300 / 350 = **43.71**

**b)** Looking at the observed counts vs. what we'd expect under independence:
- Exercisers have High Stress: observed = 25, expected ≈ 43.7 → much lower
- Non-exercisers have High Stress: observed = 65, expected ≈ 46.3 → much higher
- Exercisers have Low Stress: observed = 85, expected ≈ 60.7 → much higher

The observed and expected counts are quite **far apart**, so the chi-squared statistic would be **large**. This suggests strong evidence against independence — exercise and stress level appear to be related.

---

## TOPIC 8: ANOVA

### Solution 8.1

**a)**
- H₀: μ_A = μ_B = μ_C (the mean productivity is the same across all three programs)
- H_A: At least one mean differs from the rest

**b)** From the hint: SST = var(productivity$score) × (n−1) = var × 44 = 3590.8

- SSG = 528.4 (given)
- **SSE = SST − SSG = 3590.8 − 528.4 = 3062.4**
- df_group = k − 1 = 3 − 1 = 2
- df_residual = n − k = 45 − 3 = 42
- **MSG = SSG/df_group = 528.4/2 = 264.2**
- **MSE = SSE/df_residual = 3062.4/42 = 72.914**
- **F = MSG/MSE = 264.2/72.914 = 3.623**

Completed ANOVA table:
```
            Df  Sum Sq  Mean Sq  F value  Pr(>F)
program      2   528.4   264.2    3.623   0.032 *
Residuals   42  3062.4    72.9
```

**c)** Since the p-value = 0.032 < 0.05, we **reject H₀** at the 5% significance level. The data provides convincing evidence that at least one training program leads to a different mean productivity level than the others.

**d)** R² = SSG/SST = 528.4/3590.8 = **0.1472 ≈ 14.7%**

About 14.7% of the total variability in productivity scores is explained by the training program.

**e)** With k = 3 groups, we need C(3,2) = 3 pairwise comparisons.

Bonferroni-adjusted significance level: α* = 0.05/3 = **0.0167**

---

### Solution 8.2

**a)** SST = SSG + SSE = 450 + 13720 = **14170**

**b)** The p-value = 0.096 > 0.05. We **fail to reject** H₀. The data does not provide convincing evidence that the average differs across the four groups at the 5% significance level.

**c)** If one group mean moves closer to the overall mean while SST stays the same:
- SSG = Σ nᵢ(x̄ᵢ − x̄)² would **decrease** (less between-group variation)
- SSE = SST − SSG would **increase** (more within-group variation)
- F = (SSG/df_G) / (SSE/df_E) would **decrease** (smaller numerator, larger denominator)

---

### Solution 8.3

**ANOVA is appropriate for scenario (i).**

- **Scenario (i)**: Three independent groups, numerical response variable (blood pressure), comparing means. All ANOVA conditions can be met. ✓
- **Scenario (ii)**: **ANOVA is inappropriate** because the data is **paired/dependent** (same patients measured three times). The independence condition is violated. A repeated-measures ANOVA or paired analysis would be needed.
- **Scenario (iii)**: **ANOVA is inappropriate** because the response variable is **categorical** ("improved" / "not improved"), not numerical. A chi-squared test would be appropriate here.

---

## TOPIC 9: Linear Regression

### Solution 9.1

**a)** ŷ = 120.50 + 8.75 · size

or: rent̂ = 120.50 + 8.75 × size

**b)**
- **Intercept (120.50):** The model predicts a monthly rent of €120.50 for an apartment with 0 m². This is the baseline rent (though 0 m² is not meaningful in practice — it represents the y-intercept of the regression line).
- **Slope (8.75):** For each additional square meter of apartment size, the predicted monthly rent increases by €8.75, on average.

**c)** R² = 0.574, which means the model explains 57.4% of the variation in rent.

Since R² = r² for simple linear regression:

r = √0.574 = **0.758**

The correlation is positive (since the slope is positive), so r = +0.758.

**d)** rent̂ = 120.50 + 8.75 × 65 = 120.50 + 568.75 = **€689.25**

---

### Solution 9.2

**a)**
- **study_hours (3.21):** All else equal, each additional hour of studying is associated with an average increase of 3.21 points in the exam score.
- **sleep_hours (1.85):** All else equal, each additional hour of sleep is associated with an average increase of 1.85 points in the exam score.

**b)** The line with p-value 0.011 corresponds to sleep_hours:
- H₀: β_sleep = 0 (sleep hours has no effect on exam score, given the other variables)
- H_A: β_sleep ≠ 0

**c)** The formula for adjusted R² is:

R²_adj = 1 − [Σ(yᵢ − ŷᵢ)²/(n − k − 1)] / [Σ(yᵢ − ȳ)²/(n − 1)]

From the output: residual standard error = 8.34, df = 196
- Σ(yᵢ − ŷᵢ)²/(n − k − 1) = 8.34² = 69.556
- Σ(yᵢ − ȳ)²/(n − 1) = var(exam$score) = 118.56

R²_adj = 1 − 69.556/118.56 = 1 − 0.5867 = **0.4133**

**d)** Current model AIC = 825.4. We remove a variable if it decreases AIC, choosing the largest decrease.

- Remove study_hours → AIC = 892.1 (increase, do NOT remove)
- Remove sleep_hours → AIC = 823.8 (decrease by 1.6)
- Remove attendance → AIC = 824.1 (decrease by 1.3)

**sleep_hours** should be removed, since removing it yields the lowest AIC (823.8), which is below the current AIC of 825.4. It produces the largest decrease in AIC.

---

### Solution 9.3

**a)** For a female cat (SexM = 0, Bwt:SexM = 0):

**Ĥwt = 1.50 + 3.20 · Bwt**

**b)** For a male cat (SexM = 1):

Ĥwt = 1.50 + 3.20 · Bwt − 3.80 · 1 + 1.45 · Bwt · 1

**Ĥwt = −2.30 + 4.65 · Bwt**

**c)** The slope estimate of SexM is −3.80. This means: all else equal (same body weight), the predicted heart weight of a male cat is on average **3.80 grams lower** than that of a female cat.

*Note:* This difference is at Bwt = 0 (due to the interaction term). The interaction term (1.45) means the slope for Bwt is steeper for males, so at higher body weights, the gap narrows and eventually reverses. Specifically, for Bwt > 3.80/1.45 ≈ 2.62 kg, male cats are predicted to have higher heart weights.

---

## TOPIC 10: Logistic Regression

### Solution 10.1

**a)** The fitted model is:

log(p̂/(1 − p̂)) = 4.20 − 0.035 · income − 0.008 · credit_score + 1.25 · employment_unemployed

where p̂ is the predicted probability of default.

**b)** The odds ratio for employment (unemployed vs. employed) is:

OR = e^1.25 ≈ 3.49

**Interpretation:** All else being equal, the odds of defaulting on a loan are approximately **3.49 times higher** (or about 249% higher) for unemployed applicants compared to employed applicants.

**c)** For an unemployed applicant with income = 40 and credit_score = 650:

log-odds = 4.20 − 0.035 × 40 − 0.008 × 650 + 1.25 × 1

log-odds = 4.20 − 1.40 − 5.20 + 1.25 = **−1.15**

The log-odds of default is −1.15, which corresponds to a probability of:
p = e^(−1.15) / (1 + e^(−1.15)) = 0.3166 / 1.3166 ≈ 0.24 (24%)

---

### Solution 10.2

**a)** Sensitivity = P(Predicted Yes | Actually Yes) = TP / (TP + FN)

Sensitivity = 63 / (63 + 27) = 63/90 = **0.70**

**b)** Specificity = P(Predicted No | Actually No) = TN / (TN + FP)

Specificity = 142 / (142 + 18) = 142/160 = **0.8875**

**c)** The model with AUC = 0.84 has **better predictive accuracy**. The AUC (Area Under the ROC Curve) measures the model's ability to discriminate between positive and negative cases. A larger AUC indicates better overall predictive performance. Since 0.84 > 0.79, the first model is preferred.

---

### Solution 10.3

**a)** The missing argument is: `family = binomial`

Complete code: `model <- glm(churn ~ ., data = train_data, family = binomial)`

**b)** When using `predict(model, type = "response")`, R returns the **predicted probabilities** (values between 0 and 1) rather than the log-odds. Specifically, it computes p̂ = e^(Xβ̂) / (1 + e^(Xβ̂)), applying the inverse logit transformation to the linear predictor.

---

## TOPIC 11: Simulation-Based Inference & R Code

### Solution 11.1

```r
null_dist <- df |>
  specify(response = hand, success = "left") |>
  hypothesize(null = "point", p = 0.10) |>
  generate(reps = 1000, type = "draw") |>
  calculate(stat = "prop")
```

**Explanation:**
- `response = hand`: the variable of interest
- `success = "left"`: we count left-handed students
- `null = "point"`: testing a single proportion against a specific value
- `p = 0.10`: the hypothesized proportion under H₀
- `type = "draw"`: for point null hypotheses with a single variable, we simulate by drawing from the specified distribution
- `stat = "prop"`: we compute the sample proportion as our test statistic

---

### Solution 11.2

```r
null_dist <- voters |>
  specify(formula = preference ~ gender) |>
  hypothesize(null = "independence") |>
  generate(reps = 1000) |>
  calculate(stat = "Chisq")
```

**Explanation:**
- `preference ~ gender`: formula with response ~ explanatory
- `null = "independence"`: testing whether the two variables are independent
- `stat = "Chisq"`: the chi-squared statistic is appropriate for testing independence of two categorical variables
- For independence tests, `generate()` uses `type = "permute"` by default (randomly shuffles the explanatory variable labels)

---

### Solution 11.3

**a)** p-value = 38/1000 = **0.038**

38 out of 1000 simulated statistics were as extreme or more extreme than the observed statistic of 0.085.

**b)** Since the p-value (0.038) < α (0.05), we **reject H₀**. The data provides convincing evidence against the null hypothesis at the 5% significance level.

---

## TOPIC 12: Power & Sample Size

### Solution 12.1

For a two-sample t-test, the sample size formula is:

n ≥ (2σ₀²/δ₀²) · (z_{1−α/2} + z_{1−β})²

Given: σ₀ = 15, δ₀ = 5, α = 0.05 (two-sided → α/2 = 0.025), power = 1 − β = 0.80

From the hint:
- z₀.₉₇₅ = 1.960
- z₀.₈₀ = 0.842

n ≥ (2 × 15²/5²) × (1.960 + 0.842)²

n ≥ (2 × 225/25) × (2.802)²

n ≥ 18 × 7.851 = 141.32

Rounding up: **n = 142 participants per group** (total = 284).

---

### Solution 12.2

**a)** The output says n = 175.3847 per group. Since we can't have fractional participants, round up to 176 per group.

Total sample size = 2 × 176 = **352 participants**

**b)** The probability of detecting the effect is the **power** of the test, which was specified as **0.8 (80%)**. This means there is an 80% probability of correctly rejecting H₀ when the true effect is 3 units.

---

## TOPIC 13: Bootstrap & Confidence Intervals

### Solution 13.1

Using the bootstrap standard error method:

CI = x̄* ± z₀.₉₇₅ · SE_bootstrap

where x̄* = 15.80 (the original sample mean = the mean of bootstrap means by construction), and SE_bootstrap = 0.45.

From the hint: z₀.₉₇₅ = 1.96

CI = 15.80 ± 1.96 × 0.45 = 15.80 ± 0.882

**CI = (14.918, 16.682)** or approximately **(€14.92, €16.68)**

We are 95% confident that the true average hourly wage of part-time workers is between €14.92 and €16.68.

---

## TOPIC 14: Proportion Tests & Difference in Proportions

### Solution 14.1

**a)** Compute the sample proportions:
- p̂₁ = 72/180 = 0.400
- p̂₂ = 48/160 = 0.300

SE = √(p̂₁(1−p̂₁)/n₁ + p̂₂(1−p̂₂)/n₂)

SE = √(0.400 × 0.600/180 + 0.300 × 0.700/160)

SE = √(0.001333 + 0.001313) = √0.002646 = 0.05144

Margin of Error = z₀.₉₇₅ × SE = 1.96 × 0.05144 = **0.1008**

**b)** The confidence interval is:

(p̂₁ − p̂₂) ± ME = (0.400 − 0.300) ± 0.1008 = 0.10 ± 0.1008

CI = **(−0.0008, 0.2008)**

Since the interval **contains 0** (barely), we **cannot conclude** at the 95% confidence level that the treatment is more effective than the control. The evidence is borderline — the difference could plausibly be zero.

---

### Solution 14.2

**a)**
- H₀: p = 0.085
- H_A: p ≠ 0.085 (two-sided)

**b)** p̂ = 52/500 = 0.104

SE₀ = √(p₀(1−p₀)/n) = √(0.085 × 0.915/500) = √(0.077775/500) = √0.00015555 = 0.01247

Z = (p̂ − p₀)/SE₀ = (0.104 − 0.085)/0.01247 = 0.019/0.01247 = **1.524**

**c)** The p-value for a two-sided test = 2 × P(Z > 1.524).

From the hint: P(Z > 1.28) = 0.1003, P(Z > 1.64) = 0.0505

Since 1.28 < 1.524 < 1.64: P(Z > 1.524) is between 0.0505 and 0.1003.

So the two-sided p-value is between 0.101 and 0.201.

Since p-value > 0.05, we **fail to reject H₀**. There is not sufficient evidence at the 5% significance level to conclude that the region's unemployment rate differs from the national average.

---

## TOPIC 15: Conceptual True/False

### Solution 15.1

**a) TRUE.** A 99% CI uses a larger critical value than a 95% CI (e.g., z* = 2.576 vs. 1.96 for large samples). Since the margin of error = z* × SE, and SE is the same (same sample), the 99% CI must be wider. Higher confidence requires casting a wider net to maintain the specified coverage probability.

**b) FALSE.** The p-value is **not** the probability that H₀ is true. The p-value is the probability of observing data as extreme as (or more extreme than) what was observed, **assuming H₀ is true**. It quantifies the evidence against H₀, not the probability of H₀ being true or false. Making a statement about the probability of H₀ would require Bayesian methods with a prior distribution.

**c) FALSE.** Increasing the sample size decreases the standard error, which generally makes the test statistic larger (in absolute value) **if the effect exists**. However, if the true parameter exactly equals the null hypothesis value, increasing the sample size will NOT necessarily decrease the p-value — the test statistic will fluctuate randomly around 0, and p-values will be uniformly distributed. So the statement is only true when there is a real effect.

**d) TRUE.** A 99% CI is always wider than a 95% CI computed from the same sample (as shown in part a). Since both intervals are centered at the same point estimate, every value inside the narrower 95% CI must also be inside the wider 99% CI. The 99% CI extends further in both directions.

---

### Solution 15.2

**a) FALSE.** Rejecting H₀ in ANOVA only means that **at least one** group mean is different from the rest. It does NOT mean all means differ from each other. For example, μ_A might equal μ_B while μ_C is different. To determine which specific pairs differ, post-hoc tests (like Bonferroni-corrected pairwise t-tests or Tukey's HSD) are needed.

**b) FALSE.** A high R² only means the model explains a large proportion of variance in the response — it does not guarantee the model is appropriate. Key issues that R² does not detect:
- Non-linear relationships (residual plots may show patterns)
- Violation of normality or constant variance assumptions
- Influential outliers driving the fit
- Overfitting (especially with many predictors)

Always check residual plots regardless of R².

**c) FALSE.** The success-failure condition (np ≥ 10 and n(1−p) ≥ 10) applies specifically to the sampling distribution of a **sample proportion** (p̂), not the sample mean. For the sample mean of a general numerical variable, the relevant condition is that n should be sufficiently large (typically n ≥ 30) and the distribution should not be extremely skewed, OR the population should be approximately normal. These are different conditions.

---

*End of Solutions — All 15 Topics covered with detailed step-by-step explanations*
