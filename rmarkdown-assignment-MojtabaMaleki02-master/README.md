R Markdown Example
==================

This is a toy example to experiment with [R Markdown](https://rmarkdown.rstudio.com/). Building the example requires the following software to be installed:

* Languages:
    * [R](https://www.r-project.org/)
    * [Python](https://www.python.org/)

* R packages:
    * [rmarkdown](https://cran.r-project.org/web/packages/rmarkdown/)
    * [reticulate](https://cran.r-project.org/web/packages/reticulate/)
    * [lubridate](https://cran.r-project.org/web/packages/lubridate/)

* Python packages:
    * [wordcloud](https://pypi.org/project/wordcloud/)

* Tools:
    * [Pandoc](https://pandoc.org/)
    * [GNU Make](https://www.gnu.org/software/make/)

The easiest way of installing all required software is to use [Conda](https://docs.conda.io/en/latest/miniconda.html):

```bash
conda config --add channels conda-forge
conda config --set channel_priority strict

conda create --name rmarkdown
conda activate rmarkdown

conda install r-rmarkdown # also installs R, Pandoc, and Make
conda install r-reticulate
conda install r-lubridate
conda install wordcloud
```

To render `.Rmd` files in this folder to an output format execute the `make` command. The `make clean` command removes all files created via running `make`.