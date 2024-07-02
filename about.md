
#### **Data**

This data presents economic statistics (including median earnings, employment rates, 
gender distribution and more) for different college fields of study. The data is originally sourced 
from [American Community Survey 2010-2012 Public Use Microdata Series](https://www.census.gov/programs-surveys/acs/news/data-releases.html), with the main dataset being extracted from the [TidyTuesday GitHub Repository](https://github.com/rfordatascience/tidytuesday/tree/master/data/2018/2018-10-16).


#### **Purpose**

The purpose of the app is to:

1. provide an interactive platform for exploring economic data related to college majors and help users make informed educational/career decisions,
2. highlight majors with significant gender representation gaps, prompting users to reflect on these disparities and their implications, and
3. help users identify which college majors offer higher employment opportunities and median earnings. 

The data facilitates straightforward comparison of the number of male and female graduates across different college majors, highlighting gender representation disparities. The app also uses an interactive bubble chart to display major categories with their corresponding employment rates and median earnings, where users can gain a better perspective on how certain fields may be more in demand than others (note: size of each bubble represents total number of graduates). Finally, users can receive personalized major suggestions based on their input; recommendations also include information on median earnings, employment rates and job distributions for each relevant major.


#### **Creator**

Alexandra Goh (agoh0008@student.monash.edu)

<details>
<summary>Session information</summary>


```r
sessioninfo::session_info()
```

```
## ─ Session info ───────────────────────────────────────────────────────────────
##  setting  value
##  version  R version 4.3.3 (2024-02-29 ucrt)
##  os       Windows 11 x64 (build 22631)
##  system   x86_64, mingw32
##  ui       RStudio
##  language (EN)
##  collate  English_Malaysia.utf8
##  ctype    English_Malaysia.utf8
##  tz       Australia/Sydney
##  date     2024-05-15
##  rstudio  2024.04.1+748 Chocolate Cosmos (desktop)
##  pandoc   NA
## 
## ─ Packages ───────────────────────────────────────────────────────────────────
##  package     * version date (UTC) lib source
##  bslib         0.7.0   2024-03-29 [1] CRAN (R 4.3.3)
##  cachem        1.0.8   2023-05-01 [1] CRAN (R 4.3.1)
##  cli           3.6.2   2023-12-11 [1] CRAN (R 4.3.3)
##  colorspace    2.1-0   2023-01-23 [1] CRAN (R 4.3.2)
##  crosstalk     1.2.1   2023-11-23 [1] CRAN (R 4.3.3)
##  data.table    1.15.2  2024-02-29 [1] CRAN (R 4.3.3)
##  digest        0.6.34  2024-01-11 [1] CRAN (R 4.3.3)
##  dplyr       * 1.1.4   2023-11-17 [1] CRAN (R 4.3.3)
##  evaluate      0.23    2023-11-01 [1] CRAN (R 4.3.3)
##  fansi         1.0.6   2023-12-08 [1] CRAN (R 4.3.3)
##  farver        2.1.2   2024-05-13 [1] CRAN (R 4.3.3)
##  fastmap       1.1.1   2023-02-24 [1] CRAN (R 4.3.1)
##  forcats     * 1.0.0   2023-01-29 [1] CRAN (R 4.3.1)
##  generics      0.1.3   2022-07-05 [1] CRAN (R 4.3.1)
##  ggplot2     * 3.5.1   2024-04-23 [1] CRAN (R 4.3.3)
##  glue          1.7.0   2024-01-09 [1] CRAN (R 4.3.3)
##  gtable        0.3.5   2024-04-22 [1] CRAN (R 4.3.3)
##  hms           1.1.3   2023-03-21 [1] CRAN (R 4.3.1)
##  htmltools     0.5.8.1 2024-04-04 [1] CRAN (R 4.3.3)
##  htmlwidgets   1.6.4   2023-12-06 [1] CRAN (R 4.3.3)
##  httpuv        1.6.15  2024-03-26 [1] CRAN (R 4.3.3)
##  httr          1.4.7   2023-08-15 [1] CRAN (R 4.3.1)
##  jquerylib     0.1.4   2021-04-26 [1] CRAN (R 4.3.1)
##  jsonlite      1.8.8   2023-12-04 [1] CRAN (R 4.3.3)
##  knitr         1.46    2024-04-06 [1] CRAN (R 4.3.3)
##  labeling      0.4.3   2023-08-29 [1] CRAN (R 4.3.1)
##  later         1.3.2   2023-12-06 [1] CRAN (R 4.3.3)
##  lazyeval      0.2.2   2019-03-15 [1] CRAN (R 4.3.1)
##  lifecycle     1.0.4   2023-11-07 [1] CRAN (R 4.3.3)
##  lubridate   * 1.9.3   2023-09-27 [1] CRAN (R 4.3.1)
##  magrittr      2.0.3   2022-03-30 [1] CRAN (R 4.3.1)
##  markdown      1.12    2023-12-06 [1] CRAN (R 4.3.3)
##  memoise       2.0.1   2021-11-26 [1] CRAN (R 4.3.1)
##  mime          0.12    2021-09-28 [1] CRAN (R 4.3.0)
##  munsell       0.5.1   2024-04-01 [1] CRAN (R 4.3.3)
##  pillar        1.9.0   2023-03-22 [1] CRAN (R 4.3.1)
##  pkgconfig     2.0.3   2019-09-22 [1] CRAN (R 4.3.1)
##  plotly      * 4.10.4  2024-01-13 [1] CRAN (R 4.3.3)
##  promises      1.3.0   2024-04-05 [1] CRAN (R 4.3.3)
##  purrr       * 1.0.2   2023-08-10 [1] CRAN (R 4.3.1)
##  R6            2.5.1   2021-08-19 [1] CRAN (R 4.3.1)
##  Rcpp          1.0.12  2024-01-09 [1] CRAN (R 4.3.3)
##  readr       * 2.1.5   2024-01-10 [1] CRAN (R 4.3.3)
##  rlang         1.1.3   2024-01-10 [1] CRAN (R 4.3.3)
##  rsconnect   * 1.2.2   2024-04-04 [1] CRAN (R 4.3.3)
##  rstudioapi    0.16.0  2024-03-24 [1] CRAN (R 4.3.3)
##  sass          0.4.9   2024-03-15 [1] CRAN (R 4.3.3)
##  scales        1.3.0   2023-11-28 [1] CRAN (R 4.3.2)
##  sessioninfo   1.2.2   2021-12-06 [1] CRAN (R 4.3.1)
##  shiny       * 1.8.1.1 2024-04-02 [1] CRAN (R 4.3.3)
##  stringi       1.8.4   2024-05-06 [1] CRAN (R 4.3.3)
##  stringr     * 1.5.1   2023-11-14 [1] CRAN (R 4.3.3)
##  tibble      * 3.2.1   2023-03-20 [1] CRAN (R 4.3.1)
##  tidyr       * 1.3.1   2024-01-24 [1] CRAN (R 4.3.3)
##  tidyselect    1.2.1   2024-03-11 [1] CRAN (R 4.3.3)
##  tidyverse   * 2.0.0   2023-02-22 [1] CRAN (R 4.3.2)
##  timechange    0.3.0   2024-01-18 [1] CRAN (R 4.3.3)
##  tzdb          0.4.0   2023-05-12 [1] CRAN (R 4.3.1)
##  utf8          1.2.4   2023-10-22 [1] CRAN (R 4.3.3)
##  vctrs         0.6.5   2023-12-01 [1] CRAN (R 4.3.3)
##  viridisLite   0.4.2   2023-05-02 [1] CRAN (R 4.3.1)
##  withr         3.0.0   2024-01-16 [1] CRAN (R 4.3.3)
##  xfun          0.43    2024-03-25 [1] CRAN (R 4.3.3)
##  xtable        1.8-4   2019-04-21 [1] CRAN (R 4.3.1)
##  yaml          2.3.8   2023-12-11 [1] CRAN (R 4.3.2)
## 
##  [1] C:/Users/USER/AppData/Local/R/win-library/4.3
##  [2] C:/Program Files/R/R-4.3.3/library
## 
## ──────────────────────────────────────────────────────────────────────────────
```
</details>
