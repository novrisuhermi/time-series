# Time Series Analysis — Course Materials

Lecture notes, R code, datasets, and interactive tools for time series analysis courses taught by **Novri Suhermi** at the Department of Statistics, Institut Teknologi Sepuluh Nopember (ITS), Surabaya, Indonesia.

The materials cover classical Box–Jenkins modelling, time series econometrics, and modern forecasting with machine learning, with an emphasis on hands-on practice using real data.

---

## 📚 Courses

| Course | Focus |
|---|---|
| **Time Series Analysis** | Stationarity, ARIMA/SARIMA, model identification, diagnostics, forecasting |
| **Time Series Econometrics** | Transfer function models, intervention analysis, VAR, cointegration |
| **Forecasting with Machine Learning** (topic in *Statistical Machine Learning*) | Feature engineering for time series, tree-based and neural forecasters, backtesting |

## 🗂️ Repository Structure

```
time-series/
├── apps/            # Interactive apps
│   ├── arima-simulation/   # ARIMA simulation & case studies (HTML)
│   ├── sarima-simulation/  # SARIMA simulation & case studies (HTML)
│   ├── tf-simulation/      # Transfer function simulation & case studies (HTML)
│   └── data-generator/     # Data generator: ARIMA, SARIMA & transfer function (HTML)
├── slides/          # Lecture slides (PDF / HTML)
├── notes/           # Lecture notes and handouts
├── code/            # R scripts per topic
├── data/            # Datasets used in lectures and assignments
├── assignments/     # Problem sets and project briefs
└── README.md
```

## 🧭 Topics

1. **Foundations** — time series components, autocorrelation (ACF/PACF), white noise, stationarity and unit root tests
2. **Smoothing methods** — moving averages, exponential smoothing, Holt–Winters, ETS
3. **ARIMA modelling** — the Box–Jenkins procedure: identification, estimation, diagnostic checking, forecasting

   $$\phi_p(B)(1-B)^d Z_t = \theta_0 + \theta_q(B)\, a_t$$

4. **Seasonal ARIMA** — multiplicative SARIMA $(p,d,q)(P,D,Q)_s$
5. **Transfer function and intervention models** — modelling dynamic input–output relationships
6. **Multivariate time series** — VAR, Granger causality, cointegration, VECM
7. **Volatility models** — ARCH/GARCH for financial series
8. **Forecasting with machine learning** — lag features, tree ensembles, neural networks, rolling-origin evaluation
9. **Forecast evaluation** — MAE, RMSE, MAPE, MASE; out-of-sample validation

## 🖥️ Interactive Tools

| App | Description |
|---|---|
| [**ARIMA Simulation & Case Studies**](apps/arima-simulation/) | Simulate AR/MA/ARMA/ARIMA processes, explore ACF/PACF, and follow Box–Jenkins case studies. Runs offline in any browser. |
| [**SARIMA Simulation & Case Studies**](apps/sarima-simulation/) | Simulate seasonal ARIMA processes, explore seasonal patterns in the ACF/PACF, and follow Box–Jenkins case studies on seasonal data. Runs offline in any browser. |
| [**Transfer Function Simulation & Case Studies**](apps/tf-simulation/) | Simulate input–output systems, prewhiten series, identify $(b, r, s)$ from the CCF, and follow transfer function case studies. Runs offline in any browser. |
| [**Time Series Data Generator**](apps/data-generator/) | Generate data from ARIMA, seasonal ARIMA and transfer function models (one or several inputs) with your own sample size, orders and parameters; see the series, ACF/PACF, CCF and prewhitening, estimates against the true values and diagnostics; download CSV/Excel and the R code that reproduces the data. Runs offline in any browser. |

🌐 **Try them online:**

- ARIMA app: **https://novrisuhermi-arima.share.connect.posit.cloud**
- SARIMA app: **https://novrisuhermi-sarima.share.connect.posit.cloud**
- Transfer Function app: **https://novrisuhermi-tf.share.connect.posit.cloud**
- Data Generator app: **https://novrisuhermi-ts-sim.share.connect.posit.cloud**

## ⚙️ Getting Started

Most code is written in **R**. Install the main packages with:

```r
install.packages(c(
  "forecast", "fable", "tsibble", "feasts", "tseries",
  "urca", "vars", "rugarch", "lmtest", "ggplot2", "dplyr"
))
```

Clone the repository:

```bash
git clone https://github.com/novrisuhermi/time-series.git
```

## 📖 References

- Wei, W. W. S. (2006). *Time Series Analysis: Univariate and Multivariate Methods* (2nd ed.). Pearson.
- Box, G. E. P., Jenkins, G. M., Reinsel, G. C., & Ljung, G. M. (2015). *Time Series Analysis: Forecasting and Control* (5th ed.). Wiley.
- Hyndman, R. J., & Athanasopoulos, G. (2021). *Forecasting: Principles and Practice* (3rd ed.). OTexts. https://otexts.com/fpp3/
- Enders, W. (2014). *Applied Econometric Time Series* (4th ed.). Wiley.
- Tsay, R. S. (2010). *Analysis of Financial Time Series* (3rd ed.). Wiley.

## 👤 Instructor

**Novri Suhermi, S.Si., M.Sc.**
Department of Statistics, Institut Teknologi Sepuluh Nopember (ITS)
✉️ novri.suhermi@its.ac.id

## 📄 License

Course materials are shared under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/); code is under the [MIT License](https://opensource.org/licenses/MIT), unless stated otherwise.
