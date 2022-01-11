# DP-statistics-GWAS

This is a python code for simulation experiments on methods to release private statistics in GWAS. 
We applied the Laplace mechanism, which is based on the concept of differential privacy, to the main statistical test methods using contingency tables:
the chi-squared test, Fisher's exact test, and Cochran-Armitage's trend test. 

## the chi-squared test

For the statistics in the chi-squared test, we experimented with methods to release the p-values, log(p), chi-squared statistics when using 
2 × 2 and 3 × 2 contingency table. As for log(p), chi-squared statistics, we demonstrated the appropriate, i.e., more practical, thresholds
for several privacy levels ε in differential privacy by using simulation datasets. Detailed information on the datasets used can be found in our paper. 

## Fisher's exact test

For the Fisher's exact test, as in the case of the chi-squared test, we conducted the experiments to evaluate the utility of our proposed methods
and the thresholds for practical use of the p-values and log(p).

## Cochran-Armitage's trend test

For the Cochran-Armitage's trend test using a 3 × 2 contingency table, we focused on the chi-squared statistics and log(p). The methods of generating
the simulation data is the same as above. 

### Note

For details of the releasing methods, please see our paper entitled "More practical differentially private publication of key statistics in GWAS" (https://doi.org/10.1093/bioadv/vbab004).

