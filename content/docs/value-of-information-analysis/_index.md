# Value of Information Analysis

## Introduction
Value of information (VOI) analysis measures the value of reducing uncertainty in a cost-effectiveness or decision analysis.  VOI can be used to inform decision making, design better research studies, prioritise research more efficiently and quantify uncertainty .VOI  can be utilised to prioritise and allocate  research funding better using  costs and benefits. It is gaining increasing recognition for its utility. The costs and benefits of an intervention are weighed up alongside the value of information to reduce uncertainty.  By studying the benefits and costs of each new proposed intervention and the value of information to reduce uncertainty it becomes possible to identify topics where further research offers the greatest value. Research funders can then rank topics in order of value to determine areas of high priority. 

See also: https://www.ispor.org/heor-resources/good-practices-for-outcomes-research/article/value-of-information-analysis-for-research-decisions-an-introduction

## When might I use this?
VOI can be used in several scenarios and is becoming an increasingly utilised tool.
Eg. Funders examining a range of projects can rank the return expected from each and make funding choices from this
Eg. As an alternative to traditional methods such as power calculations to determine study sample size
Eg. Perform an economic evaluation of the next steps in a project. 

# VOI Packages

## Package: SAVI
SAVI (Sheffield Accelerated Value of Information)

Available from CRAN
(https://www.sheffield.ac.uk/polopoly_fs/1.528134!/file/Instructions_for_installing_the_SAVI_R_package.pdf) 
OR as an Rshiny server application  (http://savi.shef.ac.uk/SAVI/)

### Maintained by
Mark Strong (savi@sheffield.ac.uk)

## What does this package do?
This package can be used for :
Standardised assessment of uncertainty (C-E planes and CEACs)
Overall EVPI (Expected Value of Perfect Information) per patient, per jurisdiction per year and over your decision relevance horizon
Expected Value of Perfect Parameter Information (EVPPI) for single and groups of parameters
Also more recently they have added ability to perform risk analysis. 

## How do I input my data to it/what inputs does it take?

Rshiny application designed for only inputting PSA (probabilistic sensitivity analysis) outputs. Data can be input onto the Rshiny application as a .csv file. Either tab,comma, space or semicolon separated. On this application separate .csvs for parameters, costs and effects. 
There are also test data files on their website and github which you can practice with (https://github.com/Sheffield-Accelerated-VoI/SAVI/tree/master/test_data).
	Also requires you to fill in model parameter specifics eg. effectiveness and cost measures used 

## What outputs do I get?
Generates tabular output of and overall expected value of perfect information (EVPI), a partial EVPI for each parameter 

## Package: RANE
RANE (Rapid Assessment of Need for Evidence)
Available as an Rshiny server application (https://shiny.york.ac.uk/rane/).

No CRAN page available

## Maintained by
David Glynn (https://github.com/david-glynn)

## What does this package do?

Since this is an Rshiny application it provides an easy input page to:
1)Determining intervention with highest expected health benefit (and expected outcomes for each intervention)
2) Ascertain the value of a change in practice based on current evidence

## How do I input my data to it/what inputs does it take?
Does not appear to require user to input own files and instead requires you to fill information into boxes/drop downs  on intervention options such as baseline vs intervention, uptake, minimum clinical difference required, measurements used for endpoint, and the way the operater wants results reported. 

## What outputs do I get?
Output is in easy read format for user and and provides text on the treatment with expected highest benefit, displays expected outcomes for each treatment and the consequences of uncertainty. 

## Other packages to explore but not detailed here
The BCEA package (https://cran.r-project.org/web/packages/BCEA/BCEA.pdf) also is reportedly able to calculate VOI through removing lineard dependents in the ‘CreateInputs’ function. We could not find further information or sample code with this. 
See Probabilistic Sensitivty Analysis section of SHEPRD for more information on BCEA.

