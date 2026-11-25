# Intervention Analysis Simulation & Case Studies

An interactive, self-contained HTML app for learning Box–Tiao intervention models: an event at a known date $T$ enters an ARIMA model as a step $S_t^{(T)}$ or a pulse $P_t^{(T)}$ passed through a transfer function with delay $b$, numerator order $s$ and denominator order $r$.

$$Y_t = \sum_j \frac{\omega_j(B)}{\delta_j(B)} B^{b_j} I_{j,t} + N_t, \qquad \phi(B)\Phi(B^{s})(1-B)^d(1-B^{s})^D N_t = \theta(B)\Theta(B^{s})\, a_t$$

## Features

- Theory that follows the lecture: step and pulse inputs, reading $b$, $s$ and $r$, gain and half-life with an interactive response explorer, a gallery of nine response shapes, the eight-step modelling procedure, outliers (AO, IO, LS, TC) as intervention models, and the sign conventions of TSA, SAS and Box–Jenkins
- Eight simulations with known true effects (abrupt, gradual, delayed, temporary, temporary plus permanent, integrated noise, seasonal noise, two events), generated with R's random numbers so that the R code in the app reproduces every series exactly
- Nine case studies: 9/11 and U.S. air travel (Cryer & Chan, 2008), the UK seat-belt law of 1983, a charge for directory assistance in Cincinnati (1974), a tranquilliser and a patient's perceptual speed, a smoking ban in Victoria's gaming venues (2002), Australia's National Firearms Agreement with placebo series, the Bali bombings, COVID-19 and international arrivals to Indonesia, and the Nile at Aswan
- The same steps for every series: the pre-event ARIMA model and its no-event forecast, the response chart (forecast errors after $T$) for identifying $b$, $s$ and $r$, joint estimation, diagnostics (Ljung–Box, Jarque–Bera, residual ACF/PACF), the effect path with a 95% interval (percentages for log models), gain, half-life and cumulative effect, and R code with `TSA::arimax`
- Estimation in the browser by exact maximum likelihood (Kalman filter), a port of R's `stats::arima` and of `TSA::arimax` extended to seasonal ARIMA noise; the 9/11 model reproduces the estimates of Cryer & Chan (2008) to four decimals
- An outlier page: a Chen & Liu (1993) style search for AO, IO, LS and TC outliers when the date is unknown, with joint re-estimation
- English and Indonesian interface; equations rendered with KaTeX

## Data

`TSA::airmiles`; R `datasets::Seatbelts` and `datasets::Nile`; the Time Series Data Library (R package `tsdl`): directory assistance calls (McCleary & Hay, 1980), a schizophrenic patient's test scores (Glass, 1975), gambling expenditure in Victoria, Australian death rates (Neill & Leigh, 2008); Dinas Pariwisata Provinsi Bali, *Jumlah Wisatawan Asing ke Indonesia dan Bali, 1969–2025*. Every case study can be downloaded as CSV from the app.

## How to Use

### Online

Open the app directly in your browser: **https://novrisuhermi.github.io/apps/intervention-analysis/**

### Offline

1. Download [`Intervention_Analysis_Simulation_Case_Studies.html`](Intervention_Analysis_Simulation_Case_Studies.html) (click the file, then the **Download raw file** button).
2. Open it in any modern web browser (Chrome, Edge, Firefox, Safari).

No installation, R, or internet connection is required.
