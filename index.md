---
title: 'Tidyverse: Data wrangling & visualization'
author: Liza Wood
date: "2023-04-27"

github-repo: liza-wood/tidyverse_intro
url: "https://github.com/liza-wood/tidyverse_intro"

site: "bookdown::bookdown_site"
knit: "bookdown::render_book"

output:
  bookdown::gitbook:
    css: styling.css
    config:
      code_folding: show
      toc: 
        before: |
          <li><a href="https://allisonhorst.github.io/palmerpenguins/">
            <img src="img/lter_penguins.png" style="height: 100%; width: 100%; object-fit: contain" />
            <figcaption style="font-size: 8px">Artwork by @allison_horst</figcaption>
          </a></li>
          <li><a href="./" style="font-size: 15px">Tidyverse: Data wrangling & visualization</a></li>
        collapse: section


---

# Overview {-}

## Introduction

This tutorial is an introduction to data wrangling and visualization using functions from the `tidyverse`. It uses data from the Palmer Station's Long Term Ecological Research program based in Antarctica, including the `palmerpenguins` and weather monitoring data. These lessons walk through key steps in the data wrangling phase, including subsetting data, summarizing data at aggregate levels, creating new variables using conditional statements, working with dates, joining together multiple data frames, and reshaping data. This lesson also provides an introduction to combining data wrangling with visualization. 

**Prerequisites** 

* Installation of R and RStudio
* General knowledge of R's base functionality (math, naming objects) (note: you can familiarize yourself with R's base functionality and RStudio's layout [here](https://gge-ucd.github.io/R-DAVIS/lesson_01_intro_r_rstudio.html))


<div class="figure" style="text-align: center">
<img src="img/learning_r.png" alt="Artwork by @allison_horst" width="60%" />
<p class="caption">(\#fig:unnamed-chunk-1)Artwork by @allison_horst</p>
</div>

## Acknowledgements  

This site was developed based on material from [UC Davis's R-DAVIS course](https://gge-ucd.github.io/R-DAVIS/index.html), which draws heavily on [Carpentries](https://datacarpentry.org/R-ecology-lesson/) R lessons. Additionally, artwork is from Allison Horst ([@allison_horst](https://allisonhorst.com/)) and website styling was also based on the designs from the [Palmer Penguins package webpage](https://allisonhorst.github.io/palmerpenguins/)
