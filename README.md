**Reconstructing High-Resolution Time Series with Radial Basis Function Interpolation (RBFI)**

In many real-world datasets—especially those involving environmental sensors, tides, or even marketing data— data arrives in irregular intervals: hourly, every 5 minutes, or even daily. Missing values are also common. This creates a central challenge: how do we reconstruct a complete, high-resolution time series from fragmented and inconsistent inputs?

As an applied mathematician, I explored Radial Basis Function Interpolation (RBFI) as a solution to this problem. RBFI is a method for scattered data interpolation that uses kernel-based functions—like Gaussian, Multiquadric, or Thin Plate—centered at known data points to smoothly estimate values in between.

Why RBFI is powerful:

Kernels can be customized to match the nature of your signal.
Sliding windows make the interpolation adaptive and localized.
Its infinite-dimensional function space captures both high-frequency and low-frequency behavior, making it ideal for reconstructing complex signals like tides or sensor data.
Research Setup:

Real-world tidal height data with varying granularities and injected missing values
Tested several kernel types: Gaussian, Multiquadric, Thin Plate, and custom (e.g. Cauchy)
Sliding windows applied with multiple N-point neighborhoods
Evaluated with RMSE, Log-MSE, and a composite score: RMSE × (-Log-MSE)
Key Finding: Even with 10% or 25% of the data missing, the Multiquadric kernel with a sliding window of ~30 points reconstructed the 5-minute signal with high accuracy. And all of this is achieved without any training phase— this is a pure interpolation method, driven entirely by math.

Why this matters:

Predictive modeling: Improves input quality by filling gaps
Visualization: Produces smooth and interpretable plots
Feature engineering: Enhances time-aware machine learning pipelines
Real-time monitoring: Ensures continuity even during sensor dropouts
RBFI is not just a mathematical curiosity—it’s a trusted tool across fields like geophysics, fluid dynamics, computer graphics, and machine learning. Its ability to handle noisy, irregular, or missing data makes it indispensable in time series reconstruction.

Made by Kévi Pegoraro
https://www.linkedin.com/in/kevi-pegoraro/
