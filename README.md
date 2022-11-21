# analytics-vidhya-job-a-thon-

1. EDA Analysis involves checking the distribution of Data, containing missing values and seasonality mode.

2. Checking outliers involves First decomposing the data into seasonal, trend, and resid. Then checking the outliers in resid that lie outside the range (resid.mean() - 3*resid.std(), resid.mean() + 3*resid.std()) (Because the data follows the normal distribution)

3. Feature Engineering involves the removal of outliers by treating them as missing values.

4. To fill the missing values, I have used Prophet model. Since the Prophet model can learn the data pattern and has ability to fill the missing values.

5. I have chosen the FBPropet model because it offers a good baseline quickly, as you don't have to craft time features. Prophet makes it possible to forecast time series with almost no feature engineering and a good performance in record time.

6. To avoid overfitting, I set the parameter changepoint range to 0.8 because the model understands the last 20% of the data by it's own. Furthermore, to prevent overfitting, I set changepoint_prior_scale=0.3, n_changepoints=6 because smaller changepoints don't tend the model to overfit.

7. There is possible overfitting due to seasonality. So I set the parameter seasonality_prior_scale=1.2

8. Performed Cross Validation by taking 99.9% data for training and 0.01% for Validation
