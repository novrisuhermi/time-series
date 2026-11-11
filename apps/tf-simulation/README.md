# Transfer Function Simulation & Case Studies

An interactive, self-contained HTML app for learning transfer function models, which describe how an input series $X_t$ dynamically affects an output series $Y_t$:

$$Y_t = \frac{\omega_s(B)}{\delta_r(B)} B^b X_t + \frac{\theta_q(B)}{\phi_p(B)} a_t$$

## Features

- Simulate input–output systems with user-chosen transfer function orders $(b, r, s)$ and noise models
- Prewhiten the input and output series and read the cross-correlation function (CCF) to identify $(b, r, s)$
- Inspect impulse response weights and see how the delay, decay, and numerator terms shape them
- Walk through real-data case studies: identification, estimation, diagnostic checking (incl. Ljung–Box test), and forecasting

## How to Use

### Online

Open the app directly in your browser: **https://novrisuhermi-tf.share.connect.posit.cloud**

### Offline

1. Download [`TF_Simulation_Case_Studies.html`](TF_Simulation_Case_Studies.html) (click the file, then the **Download raw file** button).
2. Open it in any modern web browser (Chrome, Edge, Firefox, Safari).

No installation, R, or internet connection is required.
