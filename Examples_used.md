# Examples used

Here a brief guide to the many examples. There is about one example per repository for simplicity. 

## TEST2 - text book model

We start with the text book model of a culture with only states for: substrate, biomass, and reactor volume. 
This model is used in many text books and even used for mammalian cultures to explain the main ideas around 
continuous and perfusion cultivation.

* [BPL_TEST2_Batch](https://github.com/janpeter19/BPL_TEST2_Batch) - Batch cultivation
* [BPL_TEST2_Fedbatch](https://github.com/janpeter19/BPL_TEST2_Fedbatch) - Fedbatch cultivation
* [BPL_TEST2_Chemostat](https://github.com/janpeter19/BPL_TEST2_Chemostat) - Continuous cultivation
* [BPL_TEST2_Perfusion](https://github.com/janpeter19/BPL_TEST2_Perfusion) - Perfusion cultivation

Model calibration is important in practice and a basic example using Pythnon scipy optimization routine is given below. A similar structure of the notebook is found in other "calibration-notebooks".

* [BPL_TEST2_Batch_calibration](https://github.com/janpeter19/BPL_TEST2_Batch_calibration) - Batch cultivation calibration

Design space calculation is an important kind of application and basic examples are given below. Here noise is added to the measurement signal in one of the examples. 

* [BPL_TEST2_Batch_design_space](https://github.com/janpeter19/BPL_TEST2_Batch_design_space) - Batch cultivation and design space characterization

## YEAST

The next step in culture model complexity is to include by-product formation. This is important for *S cerevisiase* and *E coli* but also for CHO-cultures. We start with a yeast model and it can be run both as as batch and fedbatch here. The model also include aeration, e.g. both liquid and gasphase included.

* [BPL_YEAST_AIR_Fedbatch](https://github.com/janpeter19/BPL_YEAST_AIR_Fedbatch) - Fedbatch cultivation of yeast in an aerated reactor

The yeast model can be structured in two parts and here the details around the respiratory bottleneck is separated and different bottlenecks are investigated. This is studied in continuous cultivation and the phenomenon of multiple steady states are elucidated.

* [BPL_YEAST_O2LIM_Chemostat](https://github.com/janpeter19/BPL_YEAST_O2LIM_Chemostat) - Continuous cultivation

The yeast respiratory bottleneck model can be described in terms of constraint-based modelling. This is illustrated in the next example. The notebook include connection to a public genome based model. 

* [BPL_YEAST_COB](https://github.com/janpeter19/BPL_YEAST_COB) - Yeast and constraint-based modelling

## ECOLI

The *E coli* model below is similar to the the yeast model but also include maintenance metabolism. Although this bacteria is in many ways simpler than yeast the metabolism and growth can be more complex...

* [BPL_ECOLI_AIR_Fedbatch](https://github.com/janpeter19/BPL_ECOLI_AIR_Fedbatch) - Fedbatch cultivation of *E coli* in an aerated reactor

## CHO

The CHO-model below is also inspired by the bottleneck model of yeast above. In this model we describe both by-products lactate and ammonia and the model has two differnt bottlenecks. The maintenance metabolism is also included. The model was originally developed for fedbatch cultivation with continuous feed. 

* [BPL_CHO_Fedbatch](https://github.com/janpeter19/BPL_CHO_Fedbatch) - Fedbatch cultivation of CHO-culture

The same CHO-model can also be used to describe continuous perfusion cultivation.

* [BPL_CHO_Perfusion](https://github.com/janpeter19/BPL_CHO_Perfusion) - Perfusion cultivation of CHO-cells

## IEC

Ion exchange chromatograpy (IEC) is an important process unit to separate the product of interest from similar molecules.
Here a simplified model is used to illustrate the main principles of operation.

* [BPL_IEC](https://github.com/janpeter19/BPL_IEC) - Ion Exchange Chromatograpy operation including UV-based pooling















