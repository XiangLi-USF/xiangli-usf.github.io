---
layout: essay
type: essay
title: "Pervasive seasonal divergence in lagged responses of vegetation growth to compound drought-heat stress on the Tibetan Plateau"
# All dates must be YYYY-MM-DD format!
date: 2026-07-13
published: true

labels:
  - Compound drought-heat stress
  - Vegetation response
  - Tibetan Plateau
  - Lag response
  - SHAP
---

Li, W., Wu, X., Meng, Z., Li, X., Song, W., & Zhao, P. (2026). Pervasive seasonal divergence in lagged responses of vegetation growth to compound drought-heat stress on the Tibetan Plateau. *Frontiers in Plant Science*, 17, 1879954.

[Article Link](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2026.1879954/full)

1. [The highlight of this article](#1-the-highlight-of-this-article)
2. [Study area and data](#2-study-area-and-data)
3. [Methods](#3-methods)
4. [Key findings](#4-key-findings)
5. [Contribution and innovation](#5-contribution-and-innovation)

## 1. The highlight of this article

This article examines how vegetation on the Tibetan Plateau responds to compound drought-heat stress, with special attention to seasonal timing and lag effects. The Tibetan Plateau is warming rapidly, and vegetation responses to climate extremes may differ sharply between spring and summer because water availability, frozen soil thawing, atmospheric demand, and plant growth stages change through the growing season.

The central finding is seasonal divergence. Spring compound drought-heat stress tends to produce a delayed vegetation response, while summer stress is more immediate. This distinction matters because ecosystem vulnerability cannot be fully understood by looking only at annual averages or single-season drought indices.

## 2. Study area and data

The study covers the Tibetan Plateau, a high-elevation region with strong climatic and vegetation gradients. The analysis combines climate, vegetation, soil, and topographic variables. Compound drought-heat stress is measured with a Compound Drought-Heat Index (CDHI), constructed from precipitation and temperature information. Vegetation growth is represented with MODIS NDVI, while environmental controls include precipitation, soil moisture, radiation, temperature, evapotranspiration, vapor pressure deficit, elevation, soil texture, and vegetation type.

## 3. Methods

The analysis first estimates pixel-level relationships between CDHI and vegetation growth under different lag windows. For spring, the study evaluates response windows from 0 to 3 months. For summer, it evaluates response windows from 0 to 2 months, reflecting the expectation that vegetation responds more rapidly during the active growing season.

The paper then compares vegetation types, especially forests and grasslands, and uses XGBoost with SHAP interpretation to identify which environmental factors help explain the spatial variation in vegetation sensitivity to compound drought-heat stress.

## 4. Key findings

<img class="img-fluid" src="{{ site.baseurl }}/img/fpls2026/fpls_fig1_raw.jpg" style="width: 90%; height: auto;">

Fig. 1 shows spring lag effects. A large share of the Plateau exhibits a one-month lagged response to spring compound drought-heat stress. This suggests that spring vegetation response is mediated by delayed soil thawing, soil moisture processes, and belowground biological activity rather than being purely immediate.

<img class="img-fluid" src="{{ site.baseurl }}/img/fpls2026/fpls_fig2_raw.jpg" style="width: 90%; height: auto;">

Fig. 2 shows summer lag effects. Compared with spring, summer vegetation responses are more immediate. This makes ecological sense: summer thermal conditions are already sufficient, so vegetation becomes more directly constrained by water limitation and atmospheric drying.

<img class="img-fluid" src="{{ site.baseurl }}/img/fpls2026/fpls_fig3_raw.jpg" style="width: 90%; height: auto;">

Fig. 3 compares forests and grasslands. Grasslands show stronger and faster sensitivity to compound drought-heat stress than forests, especially in summer. This pattern is consistent with shallower rooting systems, smaller carbon reserves, and stronger dependence on near-surface water.

<img class="img-fluid" src="{{ site.baseurl }}/img/fpls2026/fpls_fig4_raw.jpg" style="width: 90%; height: auto;">

Fig. 4 identifies important spring controls using SHAP. Spring precipitation, soil moisture, and shortwave radiation are key factors. The result suggests that spring vegetation response depends on the joint availability of water and energy, with frozen soil and delayed belowground recovery shaping the lag structure.

<img class="img-fluid" src="{{ site.baseurl }}/img/fpls2026/fpls_fig5_raw.jpg" style="width: 90%; height: auto;">

Fig. 5 identifies important summer controls. Summer precipitation and evapotranspiration become more central, while spring conditions such as spring radiation, spring CDHI, spring precipitation, and spring soil moisture still appear in the summer model. This supports the idea of cross-seasonal memory: spring climate conditions can influence how vegetation responds later in summer.

## 5. Contribution and innovation

This article contributes to vegetation-climate research in three main ways.

First, it treats compound drought-heat stress as a joint hazard rather than separating drought and heat. This is important because concurrent heat and water stress can intensify vegetation impacts beyond either driver alone.

Second, it emphasizes seasonal lag structure. The study shows that spring and summer should not be treated as interchangeable growing-season periods. Spring responses are delayed by thermal and belowground constraints, while summer responses are more immediate because water limitation becomes dominant.

Third, it combines spatial correlation analysis with machine learning interpretation. XGBoost and SHAP help move beyond mapping where vegetation responds by identifying which environmental factors are associated with stronger sensitivity.

Overall, the study shows that ecosystem vulnerability on the Tibetan Plateau is shaped by timing, vegetation type, and cross-seasonal memory. This provides a more nuanced basis for predicting how high-elevation ecosystems may respond to intensifying compound climate extremes.
