# Multivariate Multiple Regression in R

Multivariate Multiple Regression is the method of modeling multiple responses, or dependent variables, with a single set of predictor variables.
Let's see an example.
```
model <- lm(cbind(Petal.Width, Petal.Length) ~ 
                Sepal.Length + Sepal.Width + Species, data = iris)
summary(model)
```


Although fitting a multivariate linear regression is more relevant that running separate univariate fits, both are conceptually same. The situation becomes interesting in the inference for the multivariate linear regression, where the responses are not independent.


The coefficients are same if we consider the multivariate model or two individual univariate models but the variance-covariance matrix of the model coefficients varies.Therefore, the coefficients from both models covary. That covariance needs to be taken into account while determining if a predictor is jointly contributing to both models.
