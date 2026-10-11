# AMS 2026: JCF Ensemble Forecasting

Code, results and slides for the talk **"A Joint Calibration–Forecast Weighting Scheme for Ensemble Forecasting of Outbreak Trajectories"** (AMS Fall 2026 Southeastern Sectional Meeting).

Raj Subedi & Gerardo Chowell, School of Public Health, Georgia State University

## What's here

- **Slides**: the talk deck (with speaker notes).
- **Code**: a copy of the [QuantDiffForecast toolbox](https://github.com/gchowell/QuantDiffForecast-Toolbox) (MATLAB) with the JCF ensemble scripts, in `forecasting_odemodels code/`.
- **Example**: simulated Ebola outbreak (`input/ebola-scenario-1.txt`); GLM, Richards and Gompertz models; 20-week calibration, 4-week forecasts, 5 rolling windows.
- **Results**: `output/`, `plots/`, `plots_jcf/`, and the summary `.csv` files.

## Run it

From `forecasting_odemodels code/` in MATLAB, in order:

```matlab
batch_GLM_ebola_scenario1; batch_RICH_ebola_scenario1; batch_GOM_ebola_scenario1
collect_metrics_simple()
create_ensemble_simple()
plot_model_fit_simple(); plot_forecasts_simple()
run_jcf_sweep()
compare_ensembles_jcf()
plot_forecasts_jcf()
```

See `JCF_pipeline_steps.docx` for details. Requires MATLAB with the Optimization, Global Optimization, and Statistics and Machine Learning toolboxes.

Contact: rsubedi1@gsu.edu · rajkumarsubedi@gmail.com
