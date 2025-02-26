# Deploying cross-language in high impact projects


The materials here support a talk at the [Spatial Data Science across
Languages (SDSL)](https://spatial-data-science.github.io/2024/)
conference 2024.

See the [slides here](slides) and in the dropdown menu above.

The quickest way to reproduce the code is probably with GitHub
codespaces or Codeanywhere, by opening the following link.

[![Open in GitHub
Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/Robinlovelace/cross_language_projects)

[![Open in Codeanywhere](https://codeanywhere.com/img/open-in-codeanywhere-btn.svg)](https://app.codeanywhere.com/#https://github.com/Robinlovelace/cross_language_projects)

See the source code at
[github.com/robinlovelace](https://github.com/Robinlovelace/cross_language_projects).

See the README for more information.

Based on
https://robinlovelace.github.io/reproducible-slides-repo-template/slides

To create your own “reproducible slides repo” follow the instructions in
the link above, starting by cloning this repo or creating a template
from this one:

``` bash
gh repo clone robinlovelace/cross_language_projects
code cross_language_projects
```

Or go to
https://github.com/Robinlovelace/reproducible-slides-repo-template and
click “Use this template”.

## Setup

To setup the repo the following commands were used

``` bash
gh repo create # create the repo on github
```

``` r
# Take snapshot with renv:
renv::snapshot()
```

Load the renv with this (also in .Rprofile):

``` r
source("renv/activate.R")
```

    - The project is out-of-sync -- use `renv::status()` for details.

``` r
# make renv pick-up rmarkdown dep:
library(rmarkdown)
library(knitr)
```

Install Python packages with:

``` r
# reticulate::install_python()
reticulate::py_install("geopandas")
```

    Using virtual environment '/home/robin/.virtualenvs/r-reticulate' ...

    + /home/robin/.virtualenvs/r-reticulate/bin/python -m pip install --upgrade --no-user geopandas

``` r
reticulate::py_install("matplotlib")
```

    Using virtual environment '/home/robin/.virtualenvs/r-reticulate' ...

    + /home/robin/.virtualenvs/r-reticulate/bin/python -m pip install --upgrade --no-user matplotlib
