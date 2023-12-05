# Saclay_Thesis_FrontPage
Script R pour générer la couverture de thèse de l'Université Paris-Saclay

_R script for generating frontpage of PhD Thesis Paris-Saclay University_

## Introduction

Le code de ce projet a été adapté à partir du projet [hadamardown](https://github.com/abichat/hadamardown), mais le rendu de `thesisdown` basé sur des templates spécifiques semble être instable et sujet à des compilations infructueuses. Ce projet a donc simplifié le template spécifiquement pour générer la couverture de thèses de doctorat personnalisées pour l'Université Paris-Saclay.

_The code for this project was adapted from the [hadamardown](https://github.com/abichat/hadamardown), but rendering `thesisdown` based on specific templates seems to be unstable and prone to unsuccessful compilations. This project has therefore simplified the template specifically to generate customized PhD thesis coverage for Paris-Saclay University._

## Utilisation _(Usage)_

Avant de démarrer le projet, assurez-vous que les dépendances sont installées, si ce n'est pas le cas, vous pouvez suivre le code suivant:

_Before starting the project, make sure all dependencies are installed. If not, you can follow the code below:_

```r
install.packages(c('tinytex', 'rmarkdown'))
tinytex::install_tinytex()
# after restarting RStudio, confirm that you have LaTeX with
tinytex:::is_tinytex()

if (!require("remotes")) 
  install.packages("remotes", repos = "https://cran.rstudio.org")
remotes::install_github("rstudio/bookdown")
remotes::install_github("ismayc/thesisdown")
remotes::install_github("abichat/hadamardown")
```

Cliquez `Saclay_Thesis_FrontPage.Rproj` pour entrer dans le projet, vous pouvez modifier les informations de couverture dans le fichier `Saclay_Thesis_FrontPage.Rmd`, y compris le titre de l'article, le résumé, le logo, etc.

_Click `Saclay_Thesis_FrontPage.Rproj` to enter the project, where you can modify the cover information in the `Saclay_Thesis_FrontPage.Rmd` file, including article title, abstract, logo, etc._

Cliquez sur le bouton `knit` dans `Rstudio` pour compiler, et lorsque la compilation est réussie, elle génère le fichier `Saclay_Thesis_FrontPage.pdf` dans le répertoire racine.

_Click the `knit` button in `Rstudio` to compile, and on successful compilation, it generates the `Saclay_Thesis_FrontPage.pdf` file in the root directory._

![img](https://www.staringatr.com/images/knitr.png?width=30pc)

## Useful resources

[Rédaction d'une thèse de doctorat à l'aide du package R `thesisdown`](https://github.com/ismayc/thesisdown)

[Template de thèse pour l'Université Paris-Saclay (`thesisdown`)](https://github.com/abichat/hadamardown)

[Template de thèse de l'université Paris Saclay (`overleaf`)](https://www.overleaf.com/latex/templates/phd-thesis-paris-saclay-university-template/ffscrjgtyxfm)

[Modèle officiel de thèse de l'Université Paris-Saclay (`latex`)](https://www.universite-paris-saclay.fr/sites/default/files/2023-02/official_template_phd_universite-paris_saclay.zip)

[Modèle officiel de thèse de l'Université Paris-Saclay (`word`)](https://www.universite-paris-saclay.fr/sites/default/files/2022-11/2022_10_31_couverture_de_these.docx)
