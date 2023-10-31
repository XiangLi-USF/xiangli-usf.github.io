---
layout: essay
type: essay
title: "Automated Glacier Snow Line Altitude Calculation Method Using Landsat Series Images in the Google Earth Engine Platform"
# All dates must be YYYY-MM-DD format!
date: 2022-05-14
published: true
labels:
  - GEE
  - Snow Line Altitude
  - High Mountain Asia
---

[Article Link](https://www.mdpi.com/2072-4292/14/10/2377)

1. [The highlight of this article](#1-the-highlight-of-this-article)
2. [Study area and dataset](#2-study-area-and-dataset)
3. [Methods](#3-methods)
4. [Results](#4-results)
5. [Some ideas for future work](#5-some-ideas-for-future-work)

## 1. The highlight of this article
* Create automated method to calculate Snow Line Altitude (SLA) on glaciers
* Explore the Google Earth Engine (GEE) ability for achieving this goal

## 2. Study area and dataset
<img class="img-" src="{{ site.baseurl }}/img/SLA/Studyarea.jpg">

We used these 12 reference glaciers to calculate SLA in this article.
The reason why we chose these glaciers is 1) each of them has more than 30 years of ongoing ELA measurements which is suitable for validation and 2) these locations are common and typical area of global mountain glaciers.

For the dataset, we used:
* Landsat Series Data: we selected all Landsat Surface Reflectance (SR) images from 1985 to 2020 in GEE.
* NASADEM: It is an relatively accurate DEM.
* Glacier Data: The outline shp and observation records.

## 3. Methods
<img class="img-" src="{{ site.baseurl }}/img/SLA/Framework.png">

[Code Link](https://code.earthengine.google.com/d9766624c4b3e7b0d84a59174ca7173a): It's shown in GEE code editer, and the language is JavaScript.

The processing can be divided into two loops.
Each year is a variable that controls the loop period in the outer loop, and all of the images are filtered and selected for calculation in the inner loop.
The algorithm can then determine the minimum SCR and maximum SLA.
The annual glacier SCR and SLA can be calculated and validated using the AAR and ELA, respectively, with these two loops.

## 4. Results
<img class="img-" src="{{ site.baseurl }}/img/SLA/SLA-Trend.jpg">
<img class="img-" src="{{ site.baseurl }}/img/SLA/SLA-Regression.jpg">

Except one glacier, others show the significantly correlates between calculation and observation.

<img class="img-" src="{{ site.baseurl }}/img/SLA/one-except.jpg">

Why did this glacier get unsuitable result is that this glacier has been experiencing accelerated mass loss for the past 40 years, with apparent variations in its length, area, and surface shape.

## 5. Some ideas for future work
(if you have interests, we can cooperate)
* Focus on some other RS dataset, because optical images are very easy to be affected by clouds and shadows.
* Debris-covered glaciers should be considered. This type of glaciers have different shapes and parameters with other mountain glaciers.
* If we can solve these problem, we could measure global mountain glaciers SLA changes and create SLA tables and datasets for each of glaciers, which should be a significantly innovation.
