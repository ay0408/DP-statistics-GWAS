# DP-statistics-GWAS

This is a python code for simulation experiments on methods to release private statistics in GWAS. 
We applied the Laplace mechanism, which is based on the concept of differential privacy, to the main statistical tests using contingency tables:
the chi-squared test, Fisher's exact test, and Cochran-Armitage's trend test. 

## the chi-squared test

For the statistics in the chi-squared test, we experimented with methods for releasing the P-values, log(P), chi-squared statistics when using 
2 × 2 and 3 × 2 contingency tables. As for log(P) and chi-squared statistics, we demonstrated the appropriate thresholds
for several privacy levels $ε$ in differential privacy by using simulation datasets. Detailed information on the datasets can be found in our paper. 

## Fisher's exact test

For the Fisher's exact test, as in the case of the chi-squared test, we conducted the experiments to evaluate the utility of our proposed methods
and the thresholds for practical use of the P-value and log(P).

## Cochran-Armitage's trend test

For the Cochran-Armitage's trend test using a 3 × 2 contingency table, we focused on the chi-squared statistics and log(P). The methods for generating
the simulation data is the same as above. 

**(2023/07) The original paper states that the Cochran-Armitage trend test has 2 degrees of freedom, which is incorrect. It has 1 degree of freedom. Accordingly, our Theorem 9 on the sensitivity of $\log_{10}$(P-value) is wrong.**  
**In the Supplementary Material, the last sentense in S1.3 is incorrect, and the discussion on Theorem S9 (= Theorem 9 in the main text) is meaningless.**  
**(Regarding the discussion on $\chi^2$-statistics, we believe it is correct as of now.)**

**<------ I uploaded the rivised version of Theorem 9 (Revised_Theorem9.pdf).**

### Major cons of our methods

・Restrictions on the number of cases and controls.

・No consideration of genome dependencies.

・The analyses for the Fisher's exact test are not rigorous. (We only considered the exact probabilities obtained from the given contingency tables. (i.e, We did not consider the effects of more extreme data than given table.)) Even under these conditions, the accuracy is not high enough.  
<----- For data with a small number of individuals, a different approach other than adding noise to the output values may by necessary.

**・Our methods for publishing log(P) in the Cochran-Armitage trend test (in the original paper) must not be used. Instead, please refer to Revised_Theorem9.pdf. In the future, while analyzing the ${\it sensitivity}$ once again (theoretically or experimentally), we plan to develop more accurate methods for publishing P-values.**

### Note

For more details, please see our paper entitled "More practical differentially private publication of key statistics in GWAS" (https://doi.org/10.1093/bioadv/vbab004) published in Bioinformatics Advances.


### Contact
Akito Yamamoto

Division of Medical Data Informatics, Human Genome Center,

the Institute of Medical Science, the University of Tokyo

a-ymmt@ims.u-tokyo.ac.jp
