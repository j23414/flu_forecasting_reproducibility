# flu_forecasting_reproducibility

Mission: Reproduce analysis with recent data

Flu forecasting analysis published in: 

* Huddleston, J., Barnes, J.R., Rowe, T., Xu, X., Kondor, R., Wentworth, D.E., Whittaker, L., Ermetal, B., Daniels, R.S., McCauley, J.W. and Fujisaki, S., 2020. Integrating genotypes and phenotypes improves long-term forecasts of seasonal influenza A/H3N2 evolution. Elife, 9, p.e60067.

Pipeline at https://github.com/blab/flu-forecasting

## Inputs

List which files need to be updated

## Run

```
git clone https://github.com/blab/flu-forecasting.git
cd flu-forecasting
# nextstrain build .  
# snakemake --use-conda --config active_builds='simulated_sample_1' -j 4
```

## Results

## Interpretation and definitions

# Antigenic drift

Antigenic novelty metric, extended from the "cross-immunity" metric from [Luksza and Lassig, 2014](https://www.nature.com/articles/nature13087). 

$$
\begin{align*}
f_i,ep(t) = \Sigma_{j:t_j< t_i} - max(x_j)exp(\frac{-D_{ep}(a_i,a_j)}{D_0}) && \text{where} && D_0=14
\end{align*}
$$