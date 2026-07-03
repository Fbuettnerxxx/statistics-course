# Introduction to Data Science and Statistical Thinking — Crash Course

Interactive, self-paced learning modules for the TUM exam (CIT5130002 / MA9712).

**Learn by doing, not by watching lectures.**

## How it works

Each module has two parts:
1. **Lesson** — Short, clear explanations with examples (no fluff)
2. **Practice** — Exam-style exercises with answer fields + reveal solutions

Open any module HTML file in your browser, read the lesson, solve the exercises, then check your answers.

## Modules

| # | Module | Topics | Time |
|---|--------|--------|------|
| 1 | [Study Design & Data Basics](modules/01_study_design.html) | Observational vs experimental, sampling, variables, descriptive stats, probability distributions, median robustness | ~35 min |
| 2 | [Probability & Bayes' Theorem](modules/02_probability_bayes.html) | Conditional probability, Bayes, independence, contingency tables, variance, covariance, Z-score | ~50 min |
| 3 | [Distributions](modules/03_distributions.html) | Binomial, Poisson, Geometric, Negative Binomial, Normal, continuous distributions, CDF, CLT | ~50 min |
| 4 | [Confidence Intervals & Hypothesis Testing](modules/04_confidence_intervals_hypothesis.html) | CI construction, bootstrap CI, t-test, p-values, proportion tests, simulation-based testing, infer workflow, power | ~60 min |
| 5 | [Chi-Squared & ANOVA](modules/05_chisquared_anova.html) | GOF, independence test, ANOVA table, Bonferroni, simulation-based chi-squared, infer workflow | ~55 min |
| 6 | [Linear Regression](modules/06_linear_regression.html) | Interpretation, R², adjusted R², AIC backward/forward selection, cross-validation, collinearity, residuals | ~55 min |
| 7 | [Classification, Bias-Variance & Logistic Regression](modules/07_logistic_regression_r.html) | KNN, bias-variance tradeoff, logistic regression, odds ratio, sensitivity/specificity, ROC/AUC, Youden's J, cross-validation | ~60 min |

## Study Plan (3 weeks to exam)

- **Week 1**: Complete all 7 modules (1 per day)
- **Week 2**: Practice with past exams, review weak areas
- **Week 3**: Full exam simulations under timed conditions

## Course Materials

The `course_materials/` folder contains the official course resources:

| Resource | Description |
|----------|-------------|
| [Course Script](course_materials/course_script.pdf) | Full lecture notes (Drton, Düker, Haug) |
| [Problems2solve](course_materials/problem_sets/problems2solve.pdf) | Course exercise sheet |
| [Problems2solve Solutions](course_materials/problem_sets/problems2solve_solutions.pdf) | Official solutions |
| [Sample Solutions](course_materials/sample_solutions/) | Problem sets 02-11 with solutions |
| [Quarto Files](course_materials/quarto_files/) | R/Quarto templates for exercises |

## Past Exams

All past exams are in the `exams/` folder for reference and practice:

| Year | Document |
|------|----------|
| 2019 | [Retake Exam](exams/2019_retake_exam.pdf) · [Solutions](exams/2019_retake_exam_solutions.pdf) |
| 2022 | [Exam](exams/2022_exam.pdf) · [Solutions](exams/2022_exam_solutions.pdf) · [Retake Solutions](exams/2022_retake_solutions.pdf) |
| 2023 | [Exam](exams/2023_exam.pdf) · [Solutions](exams/2023_exam_solutions.pdf) · [Retake Solutions](exams/2023_retake_solutions.pdf) |
| 2024 | [Data Science Exam Solutions](exams/2024_data_science_exam_solutions.pdf) |
| Practice | [Solutions (PDF)](exams/practice_solutions.pdf) · [Solutions (MD)](exams/practice_solutions.md) |

## Based on

Analysis of 8 past exams (2019-2024) + course script + exercise sheets from TUM's Introduction to Data Science and Statistical Thinking course. Every exercise mirrors the exact format, difficulty, and R output style used in the real exam.

## Contributing

Found a mistake? Want to add exercises? PRs welcome.

## License

MIT — share freely with your study group.
