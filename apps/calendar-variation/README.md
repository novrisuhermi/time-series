# Calendar Variation Simulation & Case Studies

An interactive, self-contained HTML app for learning calendar variation models: monthly series whose level moves with Islamic holidays that follow the lunar Hijri calendar (Ramadan, Idul Fitri, Idul Adha) and therefore arrive about eleven days earlier every year.

$$Y_t = \beta_0 + \beta_1 t + S_t + \sum_j \alpha_j C_{j,t} + N_t, \qquad \phi(B)\Phi(B^{12})(1-B)^d N_t = \theta(B)\Theta(B^{12})\, a_t$$

## Features

- Build calendar regressors from official Indonesian holiday dates (2004–2027): month dummies, lead–lag dummies and proportional day-level windows, including a whole-Ramadan window for Idul Fitri
- Simulate series with known day-level holiday effects, trend, seasonality and SARIMA noise, and check whether the models recover the true effects
- Walk through seven Google Trends case studies from Indonesia (kurma, peci, ketupat, sarung, sate, opor ayam, lebaran): regressors, estimation of regression models with seasonal ARIMA errors, equations, diagnostic checking (incl. Ljung–Box at seasonal and lunar lags), forecasting with 80% and 95% intervals and rolling-origin evaluation
- Compare 6 model structures × 4 calendar designs (24 models) on held-out data; upload your own monthly CSV; edit the holiday calendar
- English and Indonesian interface; equations rendered with KaTeX

## How to Use

### Online

Open the app directly in your browser: **https://novrisuhermi.github.io/apps/calendar-variation/**

### Offline

1. Download [`Calendar_Variation_Simulation_Case_Studies.html`](Calendar_Variation_Simulation_Case_Studies.html) (click the file, then the **Download raw file** button).
2. Open it in any modern web browser (Chrome, Edge, Firefox, Safari).

No installation, R, or internet connection is required.
