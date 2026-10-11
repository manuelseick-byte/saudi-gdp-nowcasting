# Forecasting Saudi Arabia's GDP

**Simon Desmet, Ali Aydin Karamustafa, and Manuel Seick**  
Barcelona School of Economics — Nowcasting & Forecasting Project, 2026

This repository documents our project on forecasting Saudi Arabia's economic activity using a mixed-frequency dynamic factor model.

## Project overview

The project studies how accurately quarterly GDP can be forecast for an oil-dependent economy with a relatively short history of complete monthly macroeconomic data.

The baseline model constructs a latent monthly factor from Saudi macroeconomic indicators and uses it to forecast quarterly real GDP growth two quarters ahead. The sample covers January 2015 to June 2026.

The extension changes the target from headline real GDP to real non-oil GDP and augments the information set with business-sentiment and financial indicators. In the project results, the factor-target correlation increases from approximately 0.53 in the baseline specification to 0.68 in the non-oil extension.

## Research design

The analysis uses a mixed-frequency dynamic factor model in the Stock-Watson tradition. Monthly and quarterly series are combined through a state-space representation and Kalman-filter-based estimation. Quarterly growth is linked to the monthly latent factor using Mariano-Murasawa aggregation.

The baseline information set includes variables capturing external conditions, oil-market developments, imports, reserves, and domestic point-of-sale activity. The extension focuses on non-oil GDP and adds PMI, the Tadawul All Share Index (TASI), and financial balance-of-payments information.

See [`methodology.md`](methodology.md) for a concise description of the modelling approach.

## Repository structure

```text
.
├── README.md
├── CITATION.cff
├── .gitignore
├── methodology.md
├── data-sources.md
├── code-availability.md
└── paper/
    └── Desmet_Karamustafa_Seick_Saudi_GDP_Forecasting.pdf
```

## Data

The project combines data from several public and institutional sources, including GASTAT, FRED, IMF International Financial Statistics, the U.S. Energy Information Administration, JODI Oil, and the Saudi Central Bank (SAMA).

The underlying data files are not redistributed in this repository. See [`data-sources.md`](data-sources.md) for the variables and source institutions used in the project.

## Code availability

The MATLAB implementation used for this course project builds on code provided as course material. For that reason, the source code is not redistributed publicly in this repository.

This repository is therefore intended as a research-project page documenting the question, methodology, data sources, and results rather than as a public replication package. See [`code-availability.md`](code-availability.md) for details.

## Main results

The baseline specification targets quarterly real GDP growth and produces a factor-target correlation of approximately 0.53.

The extension targets real non-oil GDP and adds PMI, TASI, and financial balance-of-payments information. The resulting factor has a correlation of approximately 0.68 with non-oil GDP growth, indicating stronger co-movement between the latent factor and the non-oil target series.

The project also generates two-quarter-ahead forecasts and discusses the limitations created by the short sample and Saudi Arabia's exposure to oil-market and geopolitical shocks.

## Paper

The accompanying project paper is available in [`paper/`](paper/).

## Authorship

This project was completed by Simon Desmet, Ali Aydin Karamustafa, and Manuel Seick at the Barcelona School of Economics in 2026.
