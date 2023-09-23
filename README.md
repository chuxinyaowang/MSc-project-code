# MSc-project-code
This repo is code for generating simulated frequency time-series data for both single site and genome wide frequencies.

## genome wide analysis
This folder contains genome wide simulated data generation code.
1. using 'WF_simulations.m' script to generate frequencies.
2. load 'WF_simulation_input_example.mat' to initialise all variables needed in function. And fell free to change parameters as you want to have different frequency changing situations.
3. 'plot_type_auc.m' is for comparing AUC values at different initial setitngs.
4. 'plot_genome_wide_analysis.m' is script for plotting difference boxplot and ROC plot at each individual setting.
5. For long time running and large amount of sequence, using 'HPC_running1.pbs.sh' to run ''WF_simulations.m' on HPC to do parallel computing. (Do remeber to preset initial parameters before submitting jobs on HPC)

## single_site_analysis
This folder contains single site simulated data generation code.
1. Using 'WF_single_simscp_time.m' to run single run of frequency time series (plotfig==1 for plotting time series).
2. If you want to run multiple times, using 'WF_single_timeseries.m' to run multiple times of 'WF_single_simscp_time.m' does.
3. 'plot_parameter_analysis.m' is used to obtain parameter difference plot in different regimes(s for selection coefficient, N for population size and μ for mutation rate).
4. Using 'analyse_and_save_parameters_loop.m' to store optimised parameters at each run for further analysis.
