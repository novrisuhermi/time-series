# DSARIMA Simulation & Case Studies

An interactive, self-contained HTML app for learning double seasonal ARIMA models: hourly and sub-hourly series with a daily cycle inside a weekly one.

$$\phi(B)\,\Phi(B^{s_1})\,\Omega(B^{s_2})\,(1-B)^d(1-B^{s_1})^{D_1}(1-B^{s_2})^{D_2}\,Y_t = \theta(B)\,\Theta(B^{s_1})\,\Psi(B^{s_2})\,a_t$$

## Features

- Eight simulated hourly series ($s_1 = 24$, $s_2 = 168$) with known data-generating models, generated in R (the code is shown in the app), and six case studies: electricity demand in England and Wales (Taylor, 2003) and in Victoria, pedestrian counts at two Melbourne sensors, an hourly series of the M4 competition, and call arrivals at a bank (169 five-minute intervals per day, 845 per week)
- The same steps for every series: a regression on hour-of-day and day-of-week effects (or Fourier terms), stationarity (seasonal strength of both cycles from MSTL, ADF), identification (ACF/PACF at the key lags and their satellites, a grid of 144 models), estimation, explicit equations, diagnostics (Ljung–Box at $s_1$ and $s_2$, overfitting of each of the six factors), forecasting and discussion
- Estimation by conditional sum of squares in the browser, the method of R's `arima(method = "CSS")` and SAS's METHOD=CLS, extended to two seasonal periods; for one seasonal period the estimates agree with R to about 1e-11
- Benchmarks: Taylor's double seasonal Holt–Winters (a port of `forecast::dshw()`, identical to forecast 8.21.1), seasonal naive forecasts, the regression, and the active model without its daily or weekly factor
- English and Indonesian interface; equations rendered with KaTeX

## How to Use

### Online

Open the app directly in your browser: **https://novrisuhermi.github.io/apps/dsarima/**

### Offline

1. Download [`DSARIMA_Simulation_Case_Studies.html`](DSARIMA_Simulation_Case_Studies.html) (click the file, then the **Download raw file** button).
2. Open it in any modern web browser (Chrome, Edge, Firefox, Safari).

No installation, R, or internet connection is required.
