# RationalMethod_RunoffCoefficient
Supplementary data and code: Constraints on the validity of the Rational Method for identifying peak discharge on pervious hillslopes under idealized runoff generation conditions

Contents:
* Make_Data_Runoff_Coefficient.ipynb -- program to generate data like that used in Lapides et al., 20XX. For a given saturated hydraulic conductivity (ks), sorptivity (A0), and set of climate conditions (K and b from the IFD relation I = K/D^b), a range of simulations are run to collect the necessary data to perform the Rational Method as an optimization. This is done by calculating an Intensity curve, a contributing area curve, and a runoff coefficient curve, while tracking the peak flow. Output used for publication are included in the folder titled "data." More information on the data produced by this script is included below.
* Runoff_Coefficient_Visualize_Data.ipynb -- program to visualize data output by the script Make_Data_Runoff_Coefficient.ipynb. This program plots: runoff coefficient curves under different conditions; peak flow curves under different loss scenarios; Rational Method optimizations; colorplots of runoff coefficients, peak flows, and ratio between time of concentration and critical duration. 


Data included in this repository were produced using the following parameters:

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

For those new to jupyter notebook:
Jupyter notebook is an open source python platform. Each block in the program should be run sequentially. The first block contains the dependencies for the program, which can be installed via the command line using the command: pip install DEPENDENCY. Each block includes comments that describe what is implemented in each section. Make sure file paths are set correctly before running the notebooks.


Lapides, D. A, Sytsma, A., and Thompson, S. (20XX). Constraints on the validity of the Rational Method for identifying peak discharge on pervious hillslopes under idealized runoff generation conditions. In preparation.
