# `shinytest` Template 

This template is based on [this awesome shinytest vignette](https://rstudio.github.io/shinytest/articles/ci.html) - (Updated to use `renv` instead of `packrat`).

## Configuration Steps 

- Use this template to create a new repository
- Replace `app.R` with a new shiny application
- [Follow the instructions to record a shiny test](https://rstudio.github.io/shinytest/articles/shinytest.html)
  
```
shinytest::installDependencies()
recordTest()
```

- Use [`renv::init()`](https://github.com/rstudio/renv) to track the packages used in your application

```
if (!requireNamespace("remotes"))
  install.packages("remotes")

remotes::install_github("rstudio/renv")
```

- [Follow the instructions to enable Travis CI](https://rstudio.github.io/shinytest/articles/ci.html)
- Push code changes to run a Travis build
- [Add a Travis build status badge to the README file](https://docs.travis-ci.com/user/status-images/)
