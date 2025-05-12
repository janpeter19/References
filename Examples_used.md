# Examples used

Here a brief guide to the many examples of cultures and cultivation techniques. The guide is mainly organized around the culture model used. There is about one Jupyter notebook around an example per repository.  Reference to the literature you find in the notebooks. 
I hope the variety of examples give an idea of of the versatility of using compiled Modelica code as FMU and Jupyter notebooks with small Python scripts to improve understanding of bioprocesses.

In some notebooks multiple simulations are done for sensitivity analysis, model calibration, or process optimization.  Here are used extra Python packages SALib and SciPy.  The key in these type of notebooks is that an application dependent evaluation function is defined in Python and a general flexible and open format is used and facilitated with the FMU-explore command line package. The optimization technique used is gradient free. 

There are Python techniques to parallelise computations using multiple CPU-kernels but not shown here. In the near future the updated FMI-standard 3.0 for generation of FMU provides gradient information and can be  used to make optimization more effective for a class of problems

## TEST2 

We start with the text book model of a culture with only states for: substrate, biomass, and reactor volume. 
This model is used in many text books and even used for mammalian cultures to explain the main ideas around 
continuous and perfusion cultivation.

* [BPL_TEST2_Batch](https://github.com/janpeter19/BPL_TEST2_Batch) - Batch cultivation 
* [BPL_TEST2_Fedbatch](https://github.com/janpeter19/BPL_TEST2_Fedbatch) - Fedbatch cultivation 
* [BPL_TEST2_Chemostat](https://github.com/janpeter19/BPL_TEST2_Chemostat) - Continuous cultivation 
* [BPL_TEST2_Perfusion](https://github.com/janpeter19/BPL_TEST2_Perfusion) - Perfusion cultivation

Model calibration is important in practice and a basic example using Python scipy optimization routine is given below. A similar structure of the notebook is found in other "calibration-notebooks" on this site.

* [BPL_TEST2_Batch_calibration](https://github.com/janpeter19/BPL_TEST2_Batch_calibration) - Batch cultivation calibration 

Design space calculation is an important kind of application and a basic example is given below. Here noise is added to the measurement signal in the later part of the notebook. 

* [BPL_TEST2_Batch_design_space](https://github.com/janpeter19/BPL_TEST2_Batch_design_space) - Batch cultivation and design space characterization

## YEAST

The next step in culture model complexity is to include byproduct formation. This is important for *S cerevisiase* and *E coli* and also for CHO-cultures. We start with a yeast model and it can be run both as as batch and fedbatch here. The model also includes aeration, e.g. both liquid and gasphase included. The model was originally developed for continuous cultivation.

* [BPL_YEAST_AIR_Fedbatch](https://github.com/janpeter19/BPL_YEAST_AIR_Fedbatch) - Fedbatch cultivation of yeast in an aerated reactor with DO-control 

The yeast model can be structured in two parts and here the details around the respiratory bottleneck is separated and different modifications of the bottlenecks are investigated. This is studied in continuous cultivation and the phenomenon of multiple steady states is elucidated with these model modifications. 

* [BPL_YEAST_O2LIM_Chemostat](https://github.com/janpeter19/BPL_YEAST_O2LIM_Chemostat) - Continuous cultivation - not yet public

The yeast respiratory bottleneck model can be described in terms of constraint-based modelling. This is illustrated in the next example. The notebook include connection to a public genome based model. 

* [BPL_YEAST_COB](https://github.com/janpeter19/BPL_YEAST_COB) - Yeast and constraint-based modelling

Yeast is industrially culitivated in large reactors where gradients in substrate concentration play a role for lowering yield. Reactor size typically 100 $m^3$. The inlete substrate flow gives an area of high subdtrate level and cna be percieved as a "Hot-spot". In this part of the reactor ethanol is formed while in other parts of the reactor the ethanol can be consumed during certain coditions. Here is a two-reactor setup that illustrates the phenomena.

* [BPL_YEAST_Fedbatch_hotspot](https://github.com/janpeter19/BPL_YEAST_Fedbatch_hotspot) - Yeast and fedbatch  two-reactor setup - not yet public


## ECOLI

The *E coli* model below is similar to the the yeast model but also include maintenance metabolism. Although this bacteria is in many ways simpler than yeast the metabolism and growth can be more complex in reality. The model was originally developed for fedbatch cultivation.  

* [BPL_ECOLI_AIR_Fedbatch](https://github.com/janpeter19/BPL_ECOLI_AIR_Fedbatch) - Fedbatch cultivation of *E coli* in an aerated reactor - not yet public

## CHO

The CHO-model below is also inspired by the bottleneck model of yeast above. In this model we describe both byproducts lactate and ammonia and the model has two different bottlenecks. The maintenance metabolism is also included as well as certain inhibition effects. The model was originally developed for fedbatch cultivation with continuous feed. 

* [BPL_CHO_Fedbatch](https://github.com/janpeter19/BPL_CHO_Fedbatch) - Fedbatch cultivation of CHO-culture 
* [BPL_CHO_Fedbatch_optimization](https://github.com/janpeter19/BPL_CHO_Fedbatch_optimization) - Optimization of fedbatch cultivation of CHO-culture - not yet public
* [BPL_CHO_Fedbatch_bolus](https://github.com/janpeter19/BPL_CHO_Fedbatch_bolus) - Bolus feeding of fedbatch cultivation - not yet public

The same CHO-model can also be used to describe continuous perfusion cultivation.

* [BPL_CHO_Perfusion](https://github.com/janpeter19/BPL_CHO_Perfusion) - Perfusion cultivation of CHO-cells - not yet public
* [BPL_CHO_Perfusion_cspr](https://github.com/janpeter19/BPL_CHO_Perfusion_cspr) - Perfusion cultivation of CHO-cells illustrating the CSPR concept

## FILTRATION

Separation of cells from the broth is an important process unit. The library contains a component modelling an ideal filter. This can be used  to configure perfusion cultivation as well as batch or fed-batch cultivation in sequence with a harvesting unit operation. 

A more realistic filter should model capacity degradation over time, and that may be included in the future versions of the library.

Separation of cells using a centrifuge is an interesting alternative to filtration but no model available yet. 


## CHROMATOGRAPHY

Ion exchange chromatograpy (IEC) is an important process unit to separate the product of interest from similar molecules.
Here a simplified model is used to illustrate the main principles of operation.

* [BPL_IEC_validation](https://github.com/janpeter19/BPL_IEC_validation) - Ion Exchange Chromatograpy introduction
* [BPL_IEC_operation](https://github.com/janpeter19/BPL_IEC_operation) - Ion Exchange Chromatograpy operation 
* [BPL_IEC_uv_pooling](https://github.com/janpeter19/BPL_IEC_operation) - Ion Exchange Chromatograpy using UV-pooling - not yet public 

## CONTROL AND OPERATION

The Bioprocess Library is well suited to study control and operation of a bioreactor. Here is also an ideal filter available in BPL/EquipmentLib and used in setup of perfusion cultivations. Here is also an example of downstream chromatograhy and may in the future be included BPL/EquipmentLib as a standard component. 

The bioreactor control is mainly done using PID-regulators. The BPL/Control includes a modified PID-regulator where the output signal limits can vary with time and protects the integrator from wind-up. This is important for fed-batch cultivation where process variables change considerably over time. The modified PID-regulator is built using Modelica Standard Library compomenets.

The Bioprocess Library can be used to focus simulation on details of a single unit operation. The library can also be used to simulate a small sequence of unit operations like culture expansion and culture harvest. Such operation is here modelled mainly by time schedules of signals for valves and pumps and simpler control logic. There is a possibility for more comprehensive sequence control in Modelica and may be explored in the future.
