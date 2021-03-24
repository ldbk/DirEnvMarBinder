# DirEnvMar + BinderHub !

Dépôt de cours sur les directives européennes touchant au milieu marin et leurs mises en application

# Environnement de dev basé sur Binder Hub

RStudio : [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ldbk/DirEnvMarBinder/master?urlpath=rstudio)

# Ressources

Pour le R Markdown : <https://rmarkdown.rstudio.com/lesson-15.HTML>

Pour BinderHub : <https://en.wikipedia.org/wiki/Binder_Project> 

# Short text from binder example github 

> R and RStudio in repo2docker without waiting for packages to compile!


Binder supports using R and RStudio, with libraries pinned to a specific versions.

Install R itself and your required R packages via conda packages. Installing conda packages is faster than
installing CRAN packages. This is because CRAN packages need compiling during the install process and conda
packages do not.

For some R packages there is no corresponding conda-forge package yet, in that case take a look at https://github.com/binder-examples/r. Note that these two approaches cannot be combined, so you cannot install R packages via Conda and via an `install.R` file at the same time. You can check if a required R package is available on the Conda Forge website at https://conda-forge.org/feedstocks/ by searching for `r-PACKAGENAME`. You can install R packges from other sources using a `postBuild` script.

Both [RStudio](https://www.rstudio.com/) and [IRKernel](https://irkernel.github.io/)
are installed by default, so you can use either the Jupyter notebook interface or
the RStudio interface.

# Quick and dirty recipes for Binder & RStudio

See <https://mybinder.readthedocs.io/en/latest/introduction.html>

- public repo on github
- add an runtime.txt containing the R version
- add a install.R file for the packages needed in the dev env
- apt.txt asks the install of some specific linux library
- go to <https://mybinder.org/> to prep the virutal env
- get the link and add Rstudio stuff at the end like : 
`[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/betatim/r-conda/master?urlpath=rstudio)`