# PSM
## Propensity Score Matching in R
### Introduction

Randomized controlled trials (RCTs) are considered the gold standard approach for estimating the effects of treatments, interventions, and exposures (hereafter referred to as treatments) on outcomes. Random treatment allocation ensures that treatment status will not be confounded with either measured or unmeasured baseline characteristics. (Austin, 2011)
Observational (or nonrandomized) studies draw and record the subjects according to the specific characteristics in the natural state, and describe and compare the outcomes to draw conclusions. Unlike RCTs, researchers of such research methods have no (or failed) artificial setting of characteristics of participants.
The propensity score was defined by (Rosenbaum & Rubin, 1983) to be the probability of treatment assignment conditional on observed baseline covariates: $p_i=Pr(T_i=1|X_i)$. Propensity scores are an alternative method to estimate the effect of receiving treatment when random assignment of treatments to subjects is not feasible. In practice, the propensity score is most often estimated using a logistic regression model. It is the estimate predicted probability of accepting treatment (exposure) derived from the logistic regression model.  Although logistic regression appears to be the most commonly used method for estimating the propensity score, the use of bagging or boosting, recursive partitioning or tree-based methods, random forest, and neural networks for estimating the propensity score have been examined. 
Propensity score matching (PSM) refers to the pairing of treatment and control units with similar values on the propensity score; and possibly other covariates (the characteristics of participants); and the discarding of all unmatched units.

### What is PSM in simple terms...

PSM is done on observational studies. It is done to remove the selection bias between the treatment and the control groups.
To give an example, if we want to observe the effect of the behavior of smoking on lung cancer; to judge if smoking is the only reason which influenced them to caught lung cancer; we cannot deduce this as we do not know whether the people who smoke are equivalent to the people who do not smoke. There might be other influential factors that cause lung cancer and it might not be the effect of smoking at all. In that case, we can go for a propensity score matching estimation to observe how much impact smoking had on lung cancer.

### Propensity Score Matching in R


