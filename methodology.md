# Methodology

The project uses a mixed-frequency dynamic factor model to summarise common variation across Saudi macroeconomic indicators in a latent monthly factor.

The modelling framework combines monthly indicators with quarterly GDP data in a state-space representation. The latent factor is estimated using Kalman-filter-based methods, and monthly factor estimates are aggregated to quarterly frequency using Mariano-Murasawa weights.

The baseline model targets quarterly real GDP growth. The extension changes the target to real non-oil GDP and modifies the information set to include variables expected to be more informative about non-oil activity, including PMI, the Tadawul All Share Index (TASI), and financial balance-of-payments data.

Forecasts for the next two quarters are obtained by extending the factor through the estimated state transition and mapping the quarterly factor to GDP growth.

The project is a forecasting exercise rather than a causal analysis.
