---
date: "2023-03-23"
draft: false
excerpt: The Hazards of Hazard Ratios
subtitle: "Hernán (Epidemiology, 2010)"
title: The hazards of hazard ratios
weight: 7
tags:
- statistics
- causal-inference
---


[Hernán MA. The Hazards of Hazard Ratios. Epidemiology 2010;21(1):13–5.](https://journals.lww.com/epidem/Fulltext/2010/01000/The_Hazards_of_Hazard_Ratios.4.aspx)

## Overview

The hazard ratio is often the primary effect measure reported in many epidemiologic studies. For non-time-varying binary exposures, the HR is the hazard in the exposed divided by the hazard in the unexposed. We can often think of hazards as incidence rate and thus interpret the HR as the IRR. 

Hernan states the use of the HR for causal inference is risky for two reasons. 

1. HR may change over time
2. HR has a built-in selection bias. 

In this paper, he reviews the potential issues and goes over possible solutions. 

## Motivating examplte: Women's Health Initiative (WHI)

* Randomized experiment that followed over 16,000 women for ~ 5 years. 
* Compared the risk of coronary heart disease from combined hormone therapy to placebo.
* Study halted for safety
* Primary result HR
    * A quasi-"weighted average" HR of 1.24.
    * Yearly HRs decreased over time. 

| Year   | HR   | 
| -------| -----|
| 1      | 1.81 |       
| 2      | 1.34 |       
| 3      | 1.27 |       
| 4      | 1.25 |       
| 5      | 1.45 |       
| 6      | 0.70 |
|Overall | 1.24 | 

## Problem 1--HR changes over time
* HRs change over time, but some studies only report a single HR averaged over the duration of the study's follow-up. 
* Study conclusions may vary dependent on length of follow-up
    * I feel like this is an issue for all effect measures from longitudinal studies? 
    * For example, could be HIGH risk right after initiating therapy that goes away...
* The average HR ignores the distribution of events during follow-up 
    * HR could be 1 is the hazards are identical
    * Or HR could be 1 if one hazard is higher than the other for the first half of follow-up and then lower the second half (with similar magnitudes)

So, should we restrict to period-specific HRs?

## Problem 2--period-specific HRs have a built-in selection bias. 

* If we discretize time and estimate the HR in each period $t$, we induce immortal time bias. 
    * the HR during a time period is conditional on surviving (not developing coronary heart disease) to the start of $t$. 


After year 5 the effect of hormone therapy appeared protective (HR = 0.7), indicating that the disease rate was lower in the treatment arm than in the placebo arm. 

## Is this surprising?

It shouldn't be. 
