# STATS 101B — RCBD: Jumping Duration vs Adrenaline Change

Randomized Complete Block Design (RCBD) experiment testing how **jump duration (30/60/90/120s)** affects **change in blood adrenaline (pg/mL)**, with **age** and **sex** as covariates. Full report and R workflow show significant treatment effects, strong model fit, and diagnostic support for linear modeling.

---

## What’s here
- Design: RCBD where each participant forms a block (pre–post change is the response). Treatments are fixed jump durations; age and sex included in modeling. :contentReference[oaicite:2]{index=2}
- Modeling: `lm(response ~ treatments + age + gender)` with ANOVA, post-hoc (Tukey, Fisher LSD), diagnostics, and power analysis.
- Key packages: `ggplot2`, `readxl`, `DescTools`, `agricolae`, `pwr`.

---

## Data & scripts
- Data referenced as `project.xlsx` / `project.csv` in the Rmd; keep raw data private or synthetic.
- R code demonstrates ANOVA, coefficient tables, and plots (bar w/ SE, boxplots). See figures and code snippets in the provided PDFs. 

---

## Results (short)
- **Treatments:** Highly significant differences across durations; means increase from 30s → 120s. Tukey HSD shows all pairwise contrasts significant, with the largest gap 120–30. 
- **Coefficients:** Positive slope for duration; **gender (M)** negative vs F; **age** not significant. Example fit reports **Adjusted R² ≈ 0.926**. 
- **Diagnostics:** Residuals vs Fitted and Q–Q plots acceptable (homoscedasticity/normality reasonable).
- **Post-hoc:** Fisher LSD grouping orders 120 > 90 > 60 > 30; evidence of diminishing increments (hint of plateau at higher durations). 
- **Power:** Very large observed effect; minimal per-group n needed for ≥0.95 power under adjusted effect size.

---