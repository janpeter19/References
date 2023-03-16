# Modelling used

The modelling concepts used at different levels are briefly described below. A key structure of
[Bioprocess Library *for* Modelica](https://www.openmodelica.org/images/M_images/OpenModelicaWorkshop_2021/Design%20aspects%20of%20BPL%20v4b.pdf)
is to clearly distinguish the specific application code from the general library code. 
The general code consists of models for standard equipment components like pump, tank, reactor, sensor, filter, 
as well as blocks for control systems. The equipment models are written in a general way and is 
automatically adapted to the application media used, using Modelica language concepts. The configuration 
of the process setup for batch, fedbatch, or continuos operation, and in combination with filter or chromatography step, 
is done on a high-level connecting equipment components using pipes for media and cables for signals. 
You can even model a series of processing units to simulate up-stream culture expansion as well as down-stream product harvesting.
The specific application code is written in Modelica language following a certain equation-based form. 

The application modelling consists of different parts: media, culture reactions, broth reactions, pH-buffer-reactions,
gas-liquid-transfer reactions. The example of cultures models used so far for 
[*E coli*](https://aiche.onlinelibrary.wiley.com/doi/abs/10.1021/bp9801087), 
[*S cerevisiae*](https://onlinelibrary.wiley.com/doi/10.1002/bit.260280620), 
as well as 
[CHO](https://www.sciencedirect.com/science/article/abs/pii/S1369703X12003105) 
are all based on the simplified respiratory bottleneck view of metabolism and growth.  These models 
of intermediate complexity, as well as the simplified textbook model of just substrate and cell concentrations, 
describe the culture  essentially in terms of a static function relating reactor concentrations to metabolic fluxes 
of uptake and formation rates. However, the library modelling framework allows more complex models that include dynamics 
on the cellular level as well sub-models of metabolism. 
The language [Modelica compared to SBML](https://link.springer.com/chapter/10.1007/10_2009_64)
for modelling of biological processes has some advantages. The Bioprocess Library can be used in combination with 
[constraint-based modelling](http://users.abo.fi/khaggblo/npcw21/submissions/P18_Axelsson.pdf) using Python.

The  application modelling is also used for ion-exchange-chromatography. Here the binding and convection-diffusion reactions 
are simplified to a series of tank reactors with reactions, i.e. to a set of ordinary differential equation.  A much more advanced example of using Modelica to study operation of chromatography you find
[here](https://www.mdpi.com/2227-9717/3/3/568) and indicates the potential.

The control systems used are mainly based on blocks from the Modelica Standard Library. Measurement noise is also 
added using blocks from this library. The control systems can be continuous time, including events, and regular sampled discrete time.
The application code can include tailor-made control system blocks, when needed.

The Modelica Standard Library contains comprehensive packages Fluid and Media and some ideas from these packages have served as inspiration for Bioprocess Library *for* Modelica. Bioprocess Library is so far simplified to non-compressible media and that substances are dissolved in an ideal way.  The cell concentration is viewed as a solution while it is in practice a suspension, but this is a common simplification in the field. Compatibility of Bioprocess Library *for* Modelica with MSL Fluid and Media packages has so far not been in focus.
