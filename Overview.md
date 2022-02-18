---
title: "Job Application - Data Visuals and Code"
author: "Meridith L. Bartley, PhD"
date: "2/18/2022"
output:
  html_document:
    keep_md: true
---



This document serves as application materials for the position of Data Manager/Scientist at Montana State University. It was compiled and submitted to the interview panel on 18 February, 2022. 

# Samples of Data Visualization

Three data visualization examples are included below. Two stem from research projects during my PhD in Statistics at Pennsylvania State Universities and another from a fun side project. 

## 1. Explaining a Concept

This figure is included in the publication, "Identifying and characterizing extrapolation in multivariate response data", available online [here](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0225715). 

The objective of this figure is to use a simple, yet contextually motivated, visualization to aide readers in understanding the concept of extrapolation. By using two variables from the data used in this method papers application the readers are (1) able to visualize the risk of predicting new values using model fit on specific data ranges and (2) shown why understanding extrapolation is vital using lake nutrient data that is the motivating dataset in this work. 

From this publication, 
 "When we use a model fit on available data to predict a value or values at a new location, it is important to consider how dissimilar this new observation is to previously observed values. If some or many covariate values of this new point are dissimilar enough from those used when the model was fitted (i.e. either because they are outside the range of individual covariates or because they are a novel combination of covariates) predictions at this point may be unreliable.
[This figure], adapted from work by Filstrup et al. [2], illustrates this risk with a simple linear regression between the log transformed measurements of total phosphorous (TP) and chlorophyll a (Chl a) in U.S. lakes. The data shown in blue were used to fit a linear model with the estimated regression line shown in the same color. While the selected range of data may be reasonably approximated with a linear model, the linear trend does not extend into more extreme values, and thus our model and predictions are no longer appropriate."

Code for creating this figure is available [here](https://github.com/MLBartley/MV_extrapolation/blob/master/R/06.01_visualize_ExtrapConcept.R).

Data Citation:

Soranno P., K. Cheruvelil. 2019. LAGOS-NE-LIMNO v1.087.3: A module for LAGOS-NE, a multi-scaled geospatial and temporal database of lake ecological context and water quality for thousands of U.S. Lakes: 1925-2013. Environmental Data Initiative.
https://doi.org/10.6073/pasta/08c6f9311929f4874b01bcc64eb3b2d7  

<div class="figure">
<img src="Figures/extrapolation.png" alt="A 95% confidence interval of the mean is included around the regression line. Dashed red lines represents the 95% prediction interval. Areas shaded in darker grey indicate regions of extrapolation (using the maximum leverage value (hii) to identify the boundaries)." width="100%" />
<p class="caption">A 95% confidence interval of the mean is included around the regression line. Dashed red lines represents the 95% prediction interval. Areas shaded in darker grey indicate regions of extrapolation (using the maximum leverage value (hii) to identify the boundaries).</p>
</div>


## 2. Interactive Map

This interactive map graphic was created to visualize bird satellite telemetry data. It has not be published and should not be considered a final version, rather a useful tool that can be used internally during analysis of such data. Tracking data locations have been changed as these data have not yet been published by the data providers. As such, the focus of this visual is not the data, but rather the interactive map and features themselves. Code used to create this embedded shiny app is included in this Markdown file (but not in the knitted document). Associated files (e.g. fake location data and associated .js and .css files) are also included. 

An interactive map is useful for sharing with data providers, data analysts, even the public. Errors in tracking data are not uncommon and visualizations like this making finding questionable locations easy to spot and inspect. Unlike a static map of tracking locations, this interactive graphic can easily subset data and change the focus of interest (e.g. changing variable used for coloring the locations) in real time. Long term applications of such a graphic include inclusion as a supplementary material in data and/or methods papers or even as an educational tool for the public to learn about a specific species' migration path. 





`<div style="width: 100% ; height: 700px ; text-align: center; box-sizing: border-box; -moz-box-sizing: border-box; -webkit-box-sizing: border-box;" class="muted well">Shiny applications not supported in static R Markdown documents</div>`{=html}

## 3. Learning New Skills

I also wanted to include something fun and not connected to any research! This figure was inspired by my favorite Dungeons and Dragons (DnD) podcast/show, Critical Role. This show features several voice actors (and improv geniuses!) playing years long DnD campaigns that stream live weekly. I have been watching the second campaign, "The Mighty Nein", and was inspired to create this heatmap of the use of the word "nein" throughout the many episodes. The interchangeable use of the homonyms "nein" and "nine" are used often during this campaign as both a running gag and the inspiration for the adventuring group's name (and title of this campaign), The Mighty Nein. This group typically contains 6 or 7 adventurers. Through the creation of this figure I was able to learn new R skills in web scraping of text and tables.

Code used to obtain episode transcripts and create this visual has been included in `Code/MightyNein.Rmd`. This visual serves as a fun motivation to try out new skills in R, however it could be shared with other fans of this show or as a #TidyTuesday example on Twitter. 

This work would not be possible without the availability of episode transcripts and I want to acknowledge the work of show fans in the creation of some of these transcripts available online. Transcripts of the first 42 episodes of Campaign 2 are found at Critical Role Transcripts. The CRTranscript team provided the captioning for the show through "Cornered" (2x53), when captioning was taken over by Critical Role itself using a professional transcription service.

Caveats: This figure assumes that all instances of 'nein' used in each episode are reflected in the transcripts available online. 

<div class="figure">
<img src="Figures/neinplot.png" alt="Heatmap of word use in Critical Role Campaign 2 episodes. Each gird cells represents a single episode (denoted by number text in each cell). Color represents the count of the use of the word 'nein' per episode." width="100%" />
<p class="caption">Heatmap of word use in Critical Role Campaign 2 episodes. Each gird cells represents a single episode (denoted by number text in each cell). Color represents the count of the use of the word 'nein' per episode.</p>
</div>


# Sample of Working Code 

An example of working code may be found at the GitHub repository used for storing and syncing all code related to the publication, "Identifying and characterizing extrapolation in multivariate response data".

This repository is located [here](https://github.com/MLBartley/MV_extrapolation). 



