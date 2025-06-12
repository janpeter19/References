**Note 2025-06-12**

Here is some changes in the Colab environment that makes it difficult to run the demo examples.

* PyFMI: The script setting up the environment is very slow. Loading Miniconda used to take 1-2 minuntes but now takes much longer time. Not clear why.

* FMPy: The script setting up the environment comes to a halt. Follow the instruction and restart the session.  The the script comes to a new halt. Then just choose the next cell cd BPL_ (and the address depens on the application chosen). Then choose Runtime/Run cell and below.

Further, I also gradually update the FMUs with MSL 4.1.0. For applications using PID-control that needs an update of BPL and will be done later. This updates should not affect the demo examples here. 





**Note 2025-04-dd**

The Bioprocess Library inherits some ideas from MSL Fluid and Media but is not compliant. Now here is a new repository that shows examples of how to start to combine components from the two libraries using a tailor-made adapter component for gas flows. 

* BPL\_MSL\_Adaptation - In this reposistory a MSL Boundary\_pT is with a pipe connected to a BPL ReactorAir through an adaptor component. The adaptor component translates information from the MSL Media to the BPL Media and reduced to flow and composition of the gas mixture. Information about moleculear weights of the medium species is also transferred. 

In this way by using MSL Fluid and Media we can develop gas handling before it comes to the reactor. My further idea is mainly to use the techniques here to facilitate development of BPL and how to bring in more media properties when needed.  MSL Fluid and Media contains a lot of knowledge about thermo-fluid properties of media and can be needed in futurre bioprocess applications.







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
