---
author: Catie Wiener
categories:
- SAS
date: "2023-07-07"
draft: false
excerpt: This is a class project from 2018. Using data from SurveyMonkey, I attempted to create a "point-and-click" analysis dataset and a couple of tables. 
layout: single
links:
- icon: github
  icon_pack: fab
  name: code
  url: https://github.com/ktwiener/survey-output-creation
title: SAS survey output
---

# Inspiration

This project was inspired by my time as a SAS programmer for clinical trials. It's current form works with survey data, but can be modified to work with data of other forms. It is an attempt to streamline dataset and metadata to aid in creating tables without having to modify the codebase. It does this by storing metadata information in a separate spreadsheet to be a "one source of truth". When modifications occur, this prevents having to scroll through hundreds of lines of code to find where certain labels or variable attributes need to be edited. 


# How it works

Ideally, the programs should work as-is if the directory structure is maintained. `_Create_Reports.sas` calls the SAS files in the Programs folder and the Excel spreadsheet `surveyinfo.xlsx` with metadata to create the analysis datasets and resulting tables. 

The metadata spreadsheet also has instructions for how to use the small little "package". 

Unfortunately the `ADQS.SAS` program is fairly specific to the questions we asked in our survey. Since we had a fair amount of free response, we needed a way to clean up the answers. Much of the program can probably be re-used -- the dataset is formatted following CDISC ADaM standards (or as close as I could get). 

What should actually be really useful are the table programs. I don't use SAS that much anymore, but since I'm still in courses I dabble in it some. The table programs allow for creating nice report ready tables, with the template and `PROC REPORT` code already defined. Since it's been a few years since I've used `PROC REPORT`, I know I will be using that as a resource. And the metadata comes in handy here too -- I can use the spreadsheet to assign footnotes and titles!!

#### Maybe I'll get around to posting examples/screenshots on this post, but I don't have it in me to open up SAS on my computer :) 
