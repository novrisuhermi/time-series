# Time Series Data Generator

An interactive, self-contained HTML app that generates data from ARIMA, seasonal ARIMA and transfer function models, with every setting under your control:

$$\phi_p(B)\Phi_P(B^s)(1-B)^d(1-B^s)^D Y_t = \theta_q(B)\Theta_Q(B^s)\, a_t$$

$$Y_t = c + \sum_{j} \frac{\omega_j(B)}{\delta_j(B)} B^{b_j} X_{j,t} + N_t$$

## Features

- Choose the sample size, seed, orders and parameter values: $p, d, q \le 10$ and $P, D, Q \le 5$ for (seasonal) ARIMA; one to three inputs with $b \le 5$, $r \le 2$, $s \le 5$ and an ARMA noise for transfer functions
- Live checks of stationarity, invertibility and the stability of $\delta(B)$
- Plots of the series, the differenced series, ACF and PACF against their theoretical values, inverse roots on the unit circle, $\psi$ weights, spectrum and periodogram, CCF before and after prewhitening, impulse response weights against the true ones, and the noise series
- Estimation with the numerical routines of R (`forecast::Arima`, `TSA::arimax`): estimates, standard errors, 95% intervals and whether they cover the true values, plus residual diagnostics (Ljung–Box, Jarque–Bera, McLeod–Li, $Q_0$)
- Downloads: CSV, Excel (data, model and estimates sheets), every chart as PNG or SVG, and the R code
- The same seed gives the same series in R (`set.seed()` + `arima.sim()`), so every result can be checked in R
- English and Indonesian interface

## How to Use

### Online

Open the app directly in your browser: **https://novrisuhermi-ts-sim.share.connect.posit.cloud**

### Offline

1. Download [`Time_Series_Data_Generator.html`](Time_Series_Data_Generator.html) (click the file, then the **Download raw file** button).
2. Open it in any modern web browser (Chrome, Edge, Firefox, Safari).

No installation, R, or internet connection is required.
