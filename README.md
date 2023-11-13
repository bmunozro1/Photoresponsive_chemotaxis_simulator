# Photoactivatable_chemotaxis_simulator

## theoretical_photokinetics(): Calculating theoretical photouncaging values 

This section allows for calculating theoretical photouncaging values using the following first order kinetic equation for photouncaging: 

$Y = {Y_o} + (plateau-{Y_o})(1-exp(-K*x))$

${Y_o} = 0$

Plateau = 1

**Input:** 

*   Array of x values (Dosage)
*   Photokinetic constant, k 

**Output:** 

*   Table of x and corresponding y values (normalized to 1)
*   Graph of theoretical data

## display(): Calculating kinetic constant from laboratory photokinetics data 

This section allows for calculating the photouncaging constant k using the first order kinetic equation:

$Y = {Y_o} + (plateau-{Y_o})(1-exp(-K*x))$

${Y_o} = 0$

Plateau = 1

**Input:** 


*   Excel file formatted such that the first column is labelled time and has all the time values and the corresponding y values titles labelled value.  

**Output:** 


*   Table of x and corresponding y values (normalized to 1)
*   Graph of theoretical data

## cell_movement(): Modeling cell migration

This section allows for modeling cell migration in 2D. It is based off of a stochastic compartment model developed by Fadai et al. 2019. 

**Input:** 


* V:compartment size 
* rm: motility rate between 0-1, where 1 equates to faster cells
* rp: proliferation rate between 0-1, where 1 equates to max proliferation
* rd: death rate between 0-1, where 1 equates to max death rate
* tf: final dimensionless time
* C_start: if there is a chemotactic variable applied, when is it applied.
* C_end: if there is a chemotactic variable applied, when does it end.
* rhox: how the chemotactic variable is applied over space (i.e gradient,etc)

**Output:** 


*   Graph of cell position
