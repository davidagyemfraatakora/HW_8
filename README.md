# HW8

### Question 1 (from 2020 midterm)
Using a candy dataset ([https://math.montana.edu/ahoegh/teaching/stat446/candy-data.csv](https://math.montana.edu/ahoegh/teaching/stat446/candy-data.csv)), define and fit a regression model to understand the relationship between `winpercent` and `pricepercent,` `chocolate,` and `caramel`. More insight into the data is available at [https://fivethirtyeight.com/videos/the-ultimate-halloween-candy-power-ranking/](https://fivethirtyeight.com/videos/the-ultimate-halloween-candy-power-ranking/).

a. Write out the model and define all of the coefficients. (2 points)

b. Fit the model with software of your choice and print the results. (2 points)

c. Summarize your results from part 2, in a way that Willy Wonka could understand. (2 points)

d. Using your model from part b, create the candy with the highest win percentage. Then specify the levels of the predictors and create a predictive distribution for an individual type of candy with those features. (2 points)


### Question 2 (from 2021 midterm)

a. (2 points)

Consider the code below. Create a figure of x and y. What linear regression assumption does this data violate?

```{r}
n <- 100
x <- seq(1,100, length.out = n)
sigma <- 1
beta <- c(1, 1)
x_star <- log(x)
y <- rnorm(n, beta[1] + beta[2] * x_star, sd = sigma)
combined <- tibble(y = y, x = x)
```


b. (4 points)

How well does a linear regression model (`y ~ x`) recover the point estimates of beta? Justify your answer by using several (~1000) replications of simulated data.

c. (4 points)

How well does a linear regression model capture the uncertainty in a predictions for y conditional on 

- x = 1
- x = 50
- x = 100
