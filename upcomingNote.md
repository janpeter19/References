**Note 2025-04-dd** 

* BPL\_YEAST\_AIR\_Fedbatch\_control1 - In this repository substrate feeding is controlled based on measurement of ethanol in the broth. Limitations of PID-control is illustrated. Interaction with the convetional stirrer speed control based on dissolved oxygen is also shown. 

* BPL\_YEAST\_AIR\_Fedbatch\_control2 - In this repository substrate feeding is controlled based on measurement of ethanol in the broth. Now the I-part of conventioanl PID-control is replaced with an observer of of the culture growth rate. In this way the ethanol set-point can be kept.

* BPL\_CHO\_Perfusion\_bleed\_control - The setup shows perfusion control where the bleed stream is controlled based on measurent of viability of the culture. A technique often used. 

* BPL\_CHO\_Batch\_qP\_calibration - In this example we illustrate the possilibitie to calibrate the function of recombinant protein expression $q_P()$  given that the model of cell growth and metabolism is known. Both a traditional model of $q_P()$ as a linear function with saturation, as well as a more flexible neural network model, are tested on simulated data. 


**Note 2025-02-yy** 

Here is a new repository including control design of fedbatch cultivation, made on request.
The example is about feed rate control of yeast cultivation during fedbatch with focus on 
how to address variations in the culture exponential growth rate. The analysis and the design is applicable
to control of other variables during fedbatch, like dissolved oxygen, pH etc. 

* An example of fedbatch cultivation of yeast with control of the ethanol concentration - see repository BPL\_YEAST\_Fedbatch\_control
