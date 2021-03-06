# Probabilistic Sensitivity Analysis

## Package: BCEA  

### Maintained by  
Gianluca Baio <gianluca@stats.ucl.ac.uk>  

Note information taken from these sources (Accessed 07/11/2019):  
CRAN index: https://cran.r-project.org/web/packages/hesim/index.html  
Manual:https://cran.r-project.org/web/packages/BCEA/BCEA.pdf  
Authors: Gianluca Baio, Andrea Berardi, Anna Heath  
Gian Luca’s website - http://www.statistica.it/gianluca/software/bcea/  

## What does this package do?
This package is useful for running probabilistic sensitivity analysis (PSA). Note that this package does not produce or run a base-analysis model, it is useful for  post-processing the output (e.g. plotting PSA results.  

Other functionality was not explored as part of this exercise.
  
## How do I input my data to it/what inputs does it take?
Taken from manual and example on page 11 [https://cran.r-project.org/web/packages/BCEA/BCEA.pdf]

```{bcea}
bcea(e, c, ref = 1, interventions = NULL, Kmax = 50000, wtp = NULL, plot = FALSE)
where is states
e An object containing nsim simulations for the variable of clinical effectiveness for each intervention being considered. In general it is a matrix with nsim rows and nint columns.
c An object containing nsim simulations for the variable of cost for each intervention being considered. In general it is a matrix with nsim rows and nint columns.
      	# effectiveness and cost
          ref=2, # selects the 2nd row of (e,c)
      	# as containing the reference intervention
          interventions=treats, # defines the labels to be associated
      	# with each intervention
          Kmax=50000, # maximum value possible for the willingness
      	# to pay threshold; implies that k is chosen
      	# in a grid from the interval (0,Kmax)
          plot=TRUE # plots the results
)
Inputs structure-
e
           Status Quo   Vaccination
   [1,] -0.0010466668 -0.0008986026
   [2,] -0.0008836105 -0.0007320416
c
    	Status Quo Vaccination
   [1,]  10.409146   16.252537
   [2,]   5.834875	9.373437
-          The main use for “standard” models is for PSA plots & analysis of PSA results where e and c rows represent the expected outcomes and costs from your PSA model runs e.g.
-      	e
-      	           Status Quo   Vaccination
-      	   [1,] [E(QALY) PSA outpu1] [E(QALY) PSA output 1]
-      	   [2,] [PSA output2] [PSA output 2]
-      	c
-      	  Status Quo Vaccination
-      	   [1,] [E(cost) PSA outpu1] [E(cost)PSA output 1]
-      	   [2,] [PSA output2] [PSA output 2]  
```

## What outputs do I get?
Taken from BCEA mannual - https://cran.r-project.org/web/packages/BCEA/BCEA.pdf
The output is a bcea item which is an R object containing many values including:

N.sim - Number of simulations produced by the Bayesian model
N.comparators - Number of interventions being analysed
n.comparisons- Number of possible pairwise comparisons
delta.e -For each possible comparison, the differential in the effectiveness measure
delta.c -For each possible comparison, the differential in the cost measure
ICER -The value of the Incremental Cost-Effectiveness Ratio
Kmax -The maximum value assumed for the willingness to pay threshold
k -The vector of values for the grid approximation of the willingness to pay
ceac -The value for the Cost-Effectiveness Acceptability Curve, as a function of the willingness to pay
ib-The distribution of the Incremental Benefit, for a given willingness to pay
eib- The value for the Expected Incremental Benefit, as a function of the willingness to pay
kstar- The grid approximation of the break even point(s)
best- A vector containing the numeric label of the intervention that is the most costeffective for each value of the willingness to pay in the selected grid approximation
U- An array including the value of the expected utility for each simulation from the Bayesian model, for each value of the grid approximation of the willingness to pay and for each intervention being considered
vi -An array including the value of information for each simulation from the Bayesian
model and for each value of the grid approximation of the willingness to pay
Ustar- An array including the maximum "known-distribution" utility for each simulation from the Bayesian model and for each value of the grid approximation of the willingness to pay
ol- An array including the opportunity loss for each simulation from the Bayesian model and for each value of the grid approximation of the willingness to pay
evi- The vector of values for the Expected Value of Information, as a function of the willingness to pay
interventions- A vector of labels for all the interventions considered
ref -The numeric index associated with the intervention used as reference in the analysis
comp -The numeric index(es) associated with the intervention(s) used as comparator(s) in the analysis step The step used to form the grid approximation to the willingness to pay  

## Other packages 
Not yet explored.
Stated as a functionality of hesim and heemod in their package descriptions:
https://cran.r-project.org/web/packages/heemod/heemod.pdf

Vignette for heemod PSA: https://cran.r-project.org/web/packages/heemod/vignettes/e_probabilistic.html 

https://cran.r-project.org/web/packages/hesim/hesim.pdf  

## Other helpful resources
A web-app interface of the R package - https://egon.stats.ucl.ac.uk/projects/BCEAweb/
