# Fama-French-5-factor-test- 
## Overview

The Fama-French five-factor model is widely used to explain differences in expected stock returns. However, the robustness and economic relevance of its size factor, SMB (Small Minus Big), have frequently been questioned.

This bachelor thesis reproduces the Fama-French five-factor model for US equities and examines whether incorporating firm quality into the construction of SMB can strengthen the size factor and improve the model's overall explanatory power.

The analysis covers January 1972 to December 2024.

## Research objectives

The project has three main objectives:

- Reproduce the Fama-French five-factor model using firm-level market and accounting data.

- Evaluate the reproduced model on 25 size-book-to-market test portfolios.

- Construct a quality-adjusted SMB factor and test its effect on both the size premium and the performance of the full model.

## Data

The analysis uses:

- Monthly returns for US common stocks from the CRSP database.

- Accounting data from Compustat North America.

- The one-month US Treasury bill rate and the original Fama-French factors from Kenneth French's Data Library.

- The 25 size-book-to-market portfolios from Kenneth French's Data Library for model evaluation.

The sample is restricted to common stocks listed on the NYSE, AMEX, or NASDAQ. Market and accounting data are aligned using annual June portfolio formation, following the standard Fama-French methodology.
CRSP and Compustat data are not included in this repository because they are subject to licensing restrictions.

## Methodology

### Five-factor model reproduction

The market, size, value, profitability, and investment factors were reconstructed using the Fama-French 2x3 portfolio-sorting procedure:

- MKT: market excess return

- SMB: small minus big

- HML: high minus low book-to-market ratio

- RMW: robust minus weak profitability

- CMA: conservative minus aggressive investment

The reproduced factors were compared with the original series using descriptive statistics, time-series plots, correlations, distributional comparisons, and Kolmogorov-Smirnov tests.

### Model evaluation

The reproduced five-factor model was evaluated through time-series regressions on the 25 size-book-to-market test portfolios. Model performance was assessed using portfolio alphas, alpha significance, and adjusted R-squared values.

### Quality adjustment to SMB

A firm-level quality score was constructed from three accounting measures:

- Asset turnover

- Interest coverage

- Gross profitability

Firms were ranked annually on each measure, and the three percentile rankings were combined into a single quality score. A 2x3 size-quality sort was then used to create an additional SMB component, which was incorporated into the construction of the size factor.

The original and quality-adjusted versions were compared in terms of average return, volatility, January concentration, and overall model performance.

## Main findings

The reproduction closely matched the original Fama-French factors. Each reconstructed factor had a correlation above 90% with its corresponding series from Kenneth French's Data Library.

The reproduced five-factor model explained approximately 90% of the variation in returns across the 25 test portfolios, although some portfolios retained statistically significant alphas.

The original SMB factor displayed a low average return, relatively high volatility, and a pronounced January effect.

After the quality adjustment, the mean monthly SMB return increased from 0.19% to 0.23%, while its standard deviation decreased from approximately 3.03% to 2.38%.

The difference between January and non-January SMB returns became smaller and was no longer statistically significant at the 5% level after the adjustment.

Despite improving the characteristics of SMB, the adjustment did not improve the full model. Average adjusted R-squared decreased from approximately 90.5% to 89.0%, while portfolio alphas remained broadly unchanged.

## Interpretation

The results suggest that controlling for firm quality can produce a stronger and less volatile size factor and reduce its dependence on January returns. However, improving one factor does not necessarily improve the explanatory power of the complete asset-pricing model.

The project therefore provides evidence that factor-level refinements should be evaluated not only by the behaviour of the modified factor, but also by their effect on the model as a whole.

## Full thesis

Read the complete bachelor thesis in the file: Simone_Maranta_Bachelor_Thesis.pdf

Author

Simone Maranta
Bachelor in International Economics and Finance
Bocconi University

Selected references

Fama, E. F., and French, K. R. (1993). Common Risk Factors in the Returns on Stocks and Bonds.

Fama, E. F., and French, K. R. (2015). A Five-Factor Asset Pricing Model.

Asness, C. S., Frazzini, A., Israel, R., Moskowitz, T. J., and Pedersen, L. H. (2018). Size Matters, If You Control Your Junk.

Asness, C. S., Frazzini, A., and Pedersen, L. H. (2019). Quality Minus Junk.
