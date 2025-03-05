


**Note 2025-04-xx** Recently i have developed new bioprocess examples and updated some old.

* BPL\_YEAST\_AIR\_Fedbatch - Here is now a section illustrating the impact of low dissolved oxygen levels in a homogenous bioreactor. This subject is important for understanding scale-up but clear-cut simple dynamic experiments in the lab scale are difficult to find. Instead people in the 80s and 90s focused on the more complicated two-reactor setups. 

* BPL\_YEAST\_AIR\_Fedbatch\_control1 - In this repository substrate feeding is controlled based on measurement of ethanol in the broth. Limitations of PID-control is illustrated. Interaction with the convetional stirrer speed control based on dissolved oxygen is also shown. 

* BPL\_YEAST\_AIR\_Fedbatch\_control2 - In this repository substrate feeding is controlled based on measurement of ethanol in the broth. Now the I-part of conventioanl PID-control is replaced with an observer of of the culture growth rate. In this way the ethanol set-point can be kept.


* BPL\_CHO\_Fedbatch - The model is updated and includes a state for lysed cell mass and the toxic impact that material may have on specific growth rate. Now the simulations can capture the decline of viable cell mass during later part of cultivation often found.

* BPL\_CHO\_Perfusion\_bleed\_control - The setup shows perfusion control where the bleed stream is controlled based on measurent of viability of the culture. A technique often used. 


**Note 2025-02-yy** 

Here is a new repository including control design of fedbatch cultivation, made on request.
The example is about feed rate control of yeast cultivation during fedbatch with focus on 
how to address variations in the culture exponential growth rate. The analysis and the design is applicable
to control of other variables during fedbatch, like dissolved oxygen, pH etc. 

* An example of fedbatch cultivation of yeast with control of the ethanol concentration - see repository BPL\_YEAST\_Fedbatch\_control
