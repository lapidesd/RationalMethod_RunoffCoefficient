README

This directory includes a zip file of the data used in Lapides et al., 20XX. Data were produced using the jupyter notebook in the parent directory title Make_Data_Runoff_Coefficient.ipynb with the following parameter values:

* alpha = 0.45 s/mm^1/3
* outlet = 1 mm
* xend = 100000 mm
* xtop = 0 mm
* res = 100
* ksvals = [0.05, 0.003, 0.0001, 0.0] mm/s
* bvals = [0.35, 0.425, 0.5, 0.575, 0.65]
* Kvals = [0.1, 0.5, 1.0, 5.0, 10.]
* A0vals[ks] = { 0.05: [2, 1, 0.1, 0], 0.003: [1, 0.1, 0.01, 0], 0.0001: [0.1, 0.01, 0.001, 0], 0.0: [0] }

Each csv file is titled as:

rational_info_(ks)\_(K)\_(A0)_(b).csv

Within the csv file, the columns are:

* D, Duration (s)
* tc, time of concentration for I(D) (s)
* A, contributing area for a storm of duration D and intensity I(D) (mm^2)
* I, storm intensity (mm/s)
* Q, peak flow for a storm of duration D and intensity I (mm^3/s)
* Qrat, peak flow predicted from C*A*I for each storm (mm^3/s)
* C, C3 defined in Lapides et al., 20XX -- Ctotal for a storm of intensity I and duration D = 3tc
* Creal, Ctotal defined in Lapides et al., 20XX -- ratio of total flow from the storm to total rainfall
