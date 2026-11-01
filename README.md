# Practical Machine Learning - Course Project

Predicting the quality of weight-lifting exercises (`classe` A-E) from wearable accelerometer data.

* `analysis.Rmd` - the full analysis (source)
* `analysis.html` - compiled report (created by knitting)

## Build

```r
install.packages(c("rmarkdown", "caret", "randomForest", "ggplot2"))
rmarkdown::render("analysis.Rmd")
```

The first run downloads `pml-training.csv` and `pml-testing.csv` into this folder. It also writes the 20 predictions
to `answers/problem_id_1.txt` ... `problem_id_20.txt`.

## Publish with GitHub Pages (gh-pages branch)

```bash
git init && git add analysis.Rmd analysis.html README.md
git commit -m "Add analysis"
git branch -M main
git remote add origin https://github.com/<you>/<repo>.git
git push -u origin main
git checkout -b gh-pages
git push -u origin gh-pages
```

Rename `analysis.html` to `index.html` on the `gh-pages` branch so it is served at
`https://<you>.github.io/<repo>/`.

## Data citation

Velloso, E.; Bulling, A.; Gellersen, H.; Ugulino, W.; Fuks, H. Qualitative Activity Recognition of
Weight Lifting Exercises. Proceedings of the 4th International Conference in Cooperation with SIGCHI
(Augmented Human '13). Stuttgart, Germany: ACM SIGCHI, 2013.
