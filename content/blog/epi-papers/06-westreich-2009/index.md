---
date: "2023-03-26"
draft: false
excerpt: "Invited Commentary: Positivity in Practice"
subtitle: "Westreich & Cole (AJE, 2010)"
title: Positivity in practice
weight: 6
tags:
- positivity
- causal-inference
- identification
---

_Westreich D, Cole SR. Invited Commentary: Positivity in Practice. Am J Epidemiol 2010;171(6):674–7._

## Definition of positivity
Positivity is a "necessary assumption for causal inference in observational data" that requires exposed and unexposed participants for every strata combination of the confounders. 

The authors state this formally as:

$$Pr(X=x|\textbf{Z}) > 0 \text{ where }f(\textbf{Z}) > 0$$

Plain english for my brain (maybe): This means that if a set of covariates **Z** has a probability greater than 0 in the target population, the probability of exposure x must be  greater than 0 for that particular set of covariates. 

## Types of positivity

Westreich and Cole define two types of non-positivity: deterministic and random. 

### Deterministic
**Definition**: A deterministic violation of positivity occurs when there are levels of the confounders that cannot receive a level of the exposure. The example given is the effect of hysterectomy: if we included men in our study, because they do not have uteruses (uteri?) they cannot receive the exposure level "hysterectomy" an thus positivity is violated. 

**Concern level**: Serious, can lead to nonsensical statements of effect.

**Solution**: Experienced epidemiologists should be able to avoid this type of non-positivity, by careful crafting of the sentence and target population. Restriction.

### Random
**Definition**: A random violation of positivity occurs when there are levels of the confounders without a level of the exposure by chance. This type of nonpositivty can then be classified by whether the nonpositivity is surrounded by regions of positivity. The example given in the article is grouping together ages -- there may be non-positivity in age groups 31-35 and 41-45, but positivity 36-40. It would be more comfortable to interpolate to ages 41-45 than do 31-35. 

**Concern level**: Varies. Often more difficult to assess. With continuous data, hard to avoid. Also depends on how to categorize continuous data.

**Solution**: With pockets of non-positivity, it is possible to interpolate from surrounding areas of positivity. Extrapolation not recommended. Also restriction.


## Restriction

Both positivity violations can be addressed through restriction. For deterministic non-positivity, this could be addressed via the study question and population definition. For both types, trimming and matching (via propensity scores) can remove/avoid regions of propensity score non-overlap. However, this type of restriction can alter the target population for inference. 

## More complicated topics

Time-varying non-positivity! g-estimation of a structural nested model (?) or g-computation (?) could be a way forward. 

## What we talked about

* Interpolation (pockets of non-positivity)
* The target population (how restriction will change our inference population)
    * Extended that to concepts in pharmacoepi, i.e. trimming, SMR weights
* Also some discussion about standardization vs. IPTW. Maybe need to look at a paper that discusses that more at length? 