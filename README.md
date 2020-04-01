# MAT7381 : Modèles de Régression (Hiver 2020)

Arthur Charpentier, [@freakonometrics](https://twitter.com/freakonometrics)

Plan de cours : [Plan_MAT7381_H2020pdf](docs/PlanMAT7381.pdf)

```diff
- (30 mars 2020) reprise de la session, je poste les vidéos au fur et à mesure
```

**"Notes de cours" et codes + vidéos (partie GLM) :**

- [MAT7381.html](http://freakonometrics.free.fr/MAT7381/MAT7381-H2020.html)
- (0) agenda [video](https://vimeo.com/401441666) + [pdf](/covid/GLM-0.pdf) 
- (1) lois Bernoulli, binomiale, multnomiale [video](https://vimeo.com/401464711) + [pdf](/covid/GLM-1.pdf) 
- (2) régression logistique (Bernoulli) [video](https://vimeo.com/401471254) + [pdf](/covid/GLM-2.pdf) 
- (3) régression multinomiale [video](https://vimeo.com/401971316) + [pdf](/covid/GLM-3.pdf) 
- (4) régression logistique sur variables catégorielles [video](https://vimeo.com/401969127) + [pdf](/covid/GLM-4.pdf)
- (5) régression logistique sur variables continues [video](https://vimeo.com/402262213) + [pdf](/covid/GLM-5.pdf)
- (6) analyse discriminante et courbe ROC [video](https://vimeo.com/402261818) + [pdf](/covid/GLM-6.pdf)
- (7) modèles de comptage et loi de Poisson [video](https://vimeo.com/402261657) + [pdf](/covid/GLM-7.pdf)
- (8) régression de Poisson [video](https://vimeo.com/402261431) + [pdf](/covid/GLM-8.pdf)
- (9) régression de Poisson et interprétations [video](https://vimeo.com/402630775) + [pdf](/covid/GLM-9.pdf)
- (10) régression de Poisson et méthode des marges video + [pdf](/covid/GLM-10.pdf)
- (11) régression de Poisson et application en assurance [video](https://vimeo.com/402630298) + [pdf](/covid/GLM-11.pdf)
- (12) famille exponentielle [video](https://vimeo.com/402630535) + [pdf](/covid/GLM-12.pdf)
- (13) famille exponentielle et GLM [video](https://vimeo.com/402631017) + [pdf](/covid/GLM-13.pdf)
- (14) loi et lien video [video](https://vimeo.com/402967734) + [pdf](/covid/GLM-14.pdf)
- (15) déviance et résidus [video](https://vimeo.com/402988804) + [pdf](/covid/GLM-15.pdf)
- (16) modèle Tweedie et poids [video](https://vimeo.com/403080840) + [pdf](/covid/GLM-16.pdf)
- (17) surdispersion video + [pdf](/covid/GLM-17.pdf)
- (18) tests et GLM [video](https://vimeo.com/403078679) + [pdf](/covid/GLM-18.pdf)
- (19) GLM en petite dimension [video](https://vimeo.com/403078474) + [pdf](/covid/GLM-19.pdf)
- (20) méthode stepwise [video](https://vimeo.com/403078320) + [pdf](/covid/GLM-20.pdf)
- (21) Poisson vs. Binomiale, application en démographie [video](https://vimeo.com/402928573) + [pdf](/covid/GLM-21.pdf)

**Références en R :**

- Julien Barnier, R Markdown [http://larmarange.github.io/](http://larmarange.github.io/analyse-R/rmarkdown-les-rapports-automatises.html)
- Gruber, John, Markdown: Syntax [https://daringfireball.net/](https://daringfireball.net/projects/markdown/syntax)
- Yihui Xie, J. J. Allaire & Garrett Grolemund, R Markdown: The Definitive Guide [https://bookdown.org/yihui](https://bookdown.org/yihui/rmarkdown/)
- RStudio, R Markdown [https://rmarkdown.rstudio.com/](https://rmarkdown.rstudio.com/lesson-1.html)

**Exercice :** 

- [exercices.pdf](docs/MAT7381-exercices-03012020.pdf) (et les [données](data/))
- pour ceux qui veulent se remettre en jambes en statistiques [exos-1.pdf](docs/exos-stats-2016-1.pdf) et [exos-2.pdf](docs/exos-stats-2016-2-1.pdf) 
- [devoir](https://github.com/freakonometrics/MAT7381/blob/master/devoir.md) (à rendre pour le 1er mai) 

**Examen :**

- [intra-sujet.pdf](docs/MAT7381-intra-sujet.pdf) et [intra-correction.pdf](docs/MAT7381-intra-correction.pdf)

**Données :**

``` r
Davis = read.table(
"http://socserv.socsci.mcmaster.ca/jfox/Books/Applied-Regression-2E/datasets/Davis.txt")
Davis[12,c(2,3)] = Davis[12,c(3,2)]
str(Davis)

chicago = read.table("http://freakonometrics.free.fr/chicago.txt",header=TRUE,sep=";")
str(chicago)

# install.packages(DALEX)
library(DALEX)
data(apartments, package = "DALEX")
str(apartments)
```

**Devoir : lecture d'article**

- [Candes & Tao (2005)](https://arxiv.org/pdf/math/0502327.pdf) *Decoding by Linear Programming* 
- [Aigner, Amemiya & Poirier (1976)](https://www.jstor.org/stable/2525708) *On the Estimation of Production Frontiers: Maximum Likelihood Estimation of the Parameters of a Discontinuous Density Function*
- [Atkinson & Cheng (1999)](https://link.springer.com/article/10.1023%2FA%3A1008942604045) *Computing least trimmed squares regression with the forward search*  
- [Efron, Hastie, Johnstone & Tibshirani (2004)](http://statweb.stanford.edu/~tibs/ftp/lars.pdf) *Least Angle Regression*
- [Friedman (1991)](https://projecteuclid.org/euclid.aos/1176347963) *Multivariate Adaptive Regression Splines*
- [Golub and Reinsch (1970)](https://link.springer.com/article/10.1007/BF02163027) *Singular Value Decomposition and Least Squares Solutions* (choisi)
- [Li (1991)](https://www.jstor.org/stable/2290563) *Sliced Inverse Regression for Dimension Reduction * 
- [Zhou, Li & Zhu (2013)](https://amstat.tandfonline.com/doi/abs/10.1080/01621459.2013.776499) *Tensor regression with applications in neuroimaging data analysis*
- [Wang, Meng & Tenenhaus (2009)](https://link.springer.com/chapter/10.1007%2F978-3-540-32827-8_18) *Regression Modelling Analysis on Compositional Data*  (choisi)
- [Cox (1972)](https://www.jstor.org/stable/2985181) *Regression Models and Life-Tables* (choisi)
- [Belloni, Chernozhukov & Kato (2013)](http://www.cemmap.ac.uk/wps/cwp701313.pdf) *Robust inference in high-dimensional approximately sparse quantile regression models* (choisi)
- [Best & Chakravarti N. (1990)](https://link.springer.com/article/10.1007%2FBF01580873) *Active set algorithms for isotonic regression; a unifying framework*
- [Chavez-Demoulin & Davison (2005)](https://rss.onlinelibrary.wiley.com/doi/10.1111/j.1467-9876.2005.00479.x) *Generalized additive modelling of sample extremes* (choisi)
- [Phatak & De Jong (1998)](https://onlinelibrary.wiley.com/doi/abs/10.1002/(SICI)1099-128X(199707)11:4%3C311::AID-CEM478%3E3.0.CO;2-4) *The geometry of partial least squares* (choisi)
- [Owen & Prieur (2017)](https://arxiv.org/abs/1610.02080) *On Shapley value for measuring importance of dependent inputs*
- [Fox & Monette (1990)](https://www.tandfonline.com/doi/abs/10.1080/01621459.1992.10475190) *Generalized Collinearity Diagnostics* (choisi)
  
