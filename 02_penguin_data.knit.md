# Data 

## Palmer Station penguins

The Palmer Station penguins data is a tidy data set related to three species of Antarctic penguins from Horst, Hill, and Gorman (2020)^[Horst AM, Hill AP, Gorman KB (2020). palmerpenguins: Palmer Archipelago (Antarctica) penguin data. R package version 0.1.0. https://allisonhorst.github.io/palmerpenguins/. doi: 10.5281/zenodo.3960218.].

The data contains size measurements for male and female adult foraging Adélie, Chinstrap, and Gentoo penguins observed on islands in the Palmer Archipelago near Palmer Station, Antarctica between 2007-2009. Data were collected and made available by Dr. Kristen Gorman and the Palmer Station Long Term Ecological Research (LTER) Program. You can read more about the package [here](https://allisonhorst.github.io/palmerpenguins/index.html).  

Let's start by installing the package in one of two ways:  


```r
# Install from CRAN
install.packages('palmerpenguins')
# Or install directory from the github repository
remotes::install_github("allisonhorst/palmerpenguins")
```

Now we can load in the package library, which stores the `penguins` dataset.

```r
library(palmerpenguins)
head(penguins)
```

```
## # A tibble: 6 × 8
##   species island    bill_length_mm bill_depth_mm flipper_l…¹ body_…² sex    year
##   <fct>   <fct>              <dbl>         <dbl>       <int>   <int> <fct> <int>
## 1 Adelie  Torgersen           39.1          18.7         181    3750 male   2007
## 2 Adelie  Torgersen           39.5          17.4         186    3800 fema…  2007
## 3 Adelie  Torgersen           40.3          18           195    3250 fema…  2007
## 4 Adelie  Torgersen           NA            NA            NA      NA <NA>   2007
## 5 Adelie  Torgersen           36.7          19.3         193    3450 fema…  2007
## 6 Adelie  Torgersen           39.3          20.6         190    3650 male   2007
## # … with abbreviated variable names ¹​flipper_length_mm, ²​body_mass_g
```

Learn more about each variable in the documentation

```r
?penguins
```

Let's take a look at its structure:


```r
str(penguins)
```

```
## tibble [344 × 8] (S3: tbl_df/tbl/data.frame)
##  $ species          : Factor w/ 3 levels "Adelie","Chinstrap",..: 1 1 1 1 1 1 1 1 1 1 ...
##  $ island           : Factor w/ 3 levels "Biscoe","Dream",..: 3 3 3 3 3 3 3 3 3 3 ...
##  $ bill_length_mm   : num [1:344] 39.1 39.5 40.3 NA 36.7 39.3 38.9 39.2 34.1 42 ...
##  $ bill_depth_mm    : num [1:344] 18.7 17.4 18 NA 19.3 20.6 17.8 19.6 18.1 20.2 ...
##  $ flipper_length_mm: int [1:344] 181 186 195 NA 193 190 181 195 193 190 ...
##  $ body_mass_g      : int [1:344] 3750 3800 3250 NA 3450 3650 3625 4675 3475 4250 ...
##  $ sex              : Factor w/ 2 levels "female","male": 2 1 1 NA 1 2 1 2 NA NA ...
##  $ year             : int [1:344] 2007 2007 2007 2007 2007 2007 2007 2007 2007 2007 ...
```

## Palmer Station weather 

To practice data wrangling skills, this tutorial will also use another data set from the Antarctic LTER Program -- the 'Daily averaged weather timeseries at Palmer Station, Antarctica'^[Palmer Station Antarctica LTER and P. Information Manager. 2019. Daily averaged weather timeseries (air temperature, pressure, wind speed, wind direction, precipitation, sky cover) at Palmer Station, Antarctica combining manual observations (1989 - Dec 12, 2003) and PALMOS automatic weather station measurements (Dec 13, 2003 - March 2019). ver 8. Environmental Data Initiative. https://doi.org/10.6073/pasta/cddd3985350334b876cd7d6d1a5bc7bf (Accessed 2023-03-27).], which includes various weather metrics measured between 1989-2019. We'll read in these data directly from online and name the data frame `weather`. 







