# Modelling used

The modelling concepts used at different levels are briefly described below. A key structure is
to clearly **distinguish the specific application code from the general library code**. 
The library code consists of standard equipment like: pump, tank, reactor, sensor, filter, 
as well as blocks for control system. The equipment models are written in a general way and is 
automatically adapted to the media used using Modelica language concepts. The configuration 
of the process setup is done on a high-level connecting pipes for media and cables for signals. 
The specific application code is written in Modelica language following a certain equation based form. 

The **application modelling consists of different parts** like: media, culture reactions, broth reactions, 
gas-liquid-transfer reactions. The example of cultures models used so far for 
[*E coli*](https://aiche.onlinelibrary.wiley.com/doi/abs/10.1021/bp9801087), 
[*S cerevisae*](https://onlinelibrary.wiley.com/doi/10.1002/bit.260280620), 
as well as 
[CHO](https://www.sciencedirect.com/science/article/abs/pii/S1369703X12003105) 
are all based on the simplified **respiratory bottleneck view of metabolism and growth.**  These models 
of intermediate complexity, as well as the simplified text book model, describes the culture  essentially 
in terms of a static function relating reactor concentration to metabolic fluxes of uptake and formation rate.
The modelling framwork allow more complex models that include dynamics on the cellular level.

The  application modelling is also used for ion-exchange-chromatography. Here the convection- diffusion reactions 
are simplified to a series of tank reactors with reactions, i.e. to a set of ordinary differential equation.  
