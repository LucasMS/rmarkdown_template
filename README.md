# Rmarkdown template


Rmarkdown template that uses [BiocStyle](https://bioconductor.org/packages/release/bioc/html/BiocStyle.html) with some changes in how figures are saved and displayed. For instance, `ggplot` standard palettes are changed. Contains auxiliary function to display tables using pre-set `knitr::kable()` and `DT::datatable()` configurations. 

`knit` are auxiliary bash scripts to knit the documents. For using R locally installed, use [knit_local](knit_local). For R on conda, use [knit_conda](knit_conda). There is some documentation on the scripts, so I encourage you to read it. The most common scenario is that you run [knit_local](knit_local) from your folder directory to **knit** and `Rmarkdown` that is nested somewhere in your code folder, for instance, `code/00_analysis/00_my_analysis.Rmd`.

```bash
bash knit_local code/00_analysis/00_my_analysis.Rmd
```

The outputs (html and figures) will be created in the output directory called after the Rmd path, `results/00_analysis/`. Figures are named after chunk names and the html file gets the name of the Rmd, in this case, `00_my_analysis.html`.

As any Rmd, you can always knit it from your IDE (Rstudio, for example). In these case, the outputs will be in the folder of the `Rmd`, which is not the ideal ;).

# To-do
- Parameterize knit script.
