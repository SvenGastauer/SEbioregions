Steps:

prepare and link all data R files: Catch.Rmd; ... forward: catch dataset will be updated and CTD and acustic data will be corrected/calibrated by CSIRO
note: should catches be transformed into abundances - e.g. should we take into account morphospecies' catchability etc. and rescale catches in terms of abundances? This might be important to make sure that we are working with the same units when comparing/linking catch with bioacoustic data.

run manyglm model R files: Traits_first.Rmd forward: rerun with updated data. rename the code. note: manyglm model informs Foster's model (e.g. it's used to define variables that are influential and thus need to be included in Foster's model).

split manyglm model into 2: environment and acoustic. run all three versions (enviro, acoustic and enviro+acoustic). R file: Traits_first.Rmd forward: to do

estimate variance forward: to do

kriging of all covariates used in manyglm model R file: krig_CTD.Rmd forward: krig acoustic covariates to get the same resolution and spatial coverage (polygon) than CTD data

run Foster's model using the new expanded dataset (after kriging) and considering only covariates identified in manyglm model. Make predictions and maps of spatial distribution of catches. Select a set of 'interesting' morphospecies for which maps will be shown. r file: Sven already did some of this steps forward: talk with Scott F.

develop ideas and applications:

inform active management: how do these maps change if we use enviro data from climate models or satellite as covariates? Can we use this approach to explore distributions patterns at different and possible/future enviro conditions, and thus to inform active management? in this regards, it'd be great if we had at least 1 commercially important morphospecies. Can we provide a generalised code to play with as supplementary?

link bioacoustic with catch data. by linking bioacoustic with catch data (manyglm model) we 1) test the bioacoustic data, and 2) increase our ability/confidence in predicting abundances when only bioacustic info is available (?? need to be reformulated)