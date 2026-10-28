**Note 2026-10-dd**
The following maintenance work has been done. The setup of fmpy notebooks are now done more consistently with "uv pip" and improves the setup speed. Further all setup-files have at the end a clean-up section to delete not necessary variables in the workspace after the fmu_explore class module has been populated with this context information about the application. And that item is now called Application (previously called Adapted). Finally here is progress with using the rudimentary module for OMSimulator and a handful of applications can be run. Good to see that **OMSimulator** handle well also the applications that fmpy has documented problems with! 



**Note 2026-10-05**
I have developed a first prototype fmu_explore_oms that provide the interace also to OMSimulator.
It is not complete and you only have the functions: par(), init(), newplot(), and simu() at the moment.
Further, the simu() function does not include 'cont'. You can find test notebooks for just a few applications so far BPL_TEST2_Batch, BPL_TEST2_Fedbatch. For the near future the aim is mianly to get this module comparable with the other two. In the longer perspective it would be interesting to expand the usage of FMU_explore to applications with two or more FMUs in combination and here OMSimulator has advantages compared to the other two simulator-enginges.




**Note 2026-09-28**
Now all applications have been run using **FMU\_explore version 1.2.4** and with the new **default VM Ubuntu 24.04.5 LTS**.
The setup-files for each application are also polished to the Python standard. The latest versions of PyFMI and FMPy have generally been used. However, for FMPy the older version 0.3.29 was needed for two applications as before. I will try to get the developers attention since might be important more generally.


**Note 2025-mm-dd**

The Bioprocess Library inherits some ideas from MSL Fluid and Media but is not compliant. Now here is a new repository that shows examples of how to start to combine components from the two libraries using a tailor-made adapter component for gas flows. 

* BPL\_MSL\_Adaptation - In this reposistory a MSL Boundary\_pT is with a pipe connected to a BPL ReactorAir through an adaptor component. The adaptor component translates information from the MSL Media to the BPL Media and reduced to flow and composition of the gas mixture. Information about moleculear weights of the medium species is also transferred. 

In this way by using MSL Fluid and Media we can develop gas handling before it comes to the reactor. My further idea is mainly to use the techniques here to facilitate development of BPL and how to bring in more media properties when needed.  MSL Fluid and Media contains a lot of knowledge about thermo-fluid properties of media and can be needed in futurre bioprocess applications.


**Note 2025-mm-dd** 

* BPL\_YEAST\_AIR\_Fedbatch\_control1 - In this repository substrate feeding is controlled based on measurement of ethanol in the broth. Limitations of PID-control is illustrated. Interaction with the convetional stirrer speed control based on dissolved oxygen is also shown. 

* BPL\_YEAST\_AIR\_Fedbatch\_control2 - In this repository substrate feeding is controlled based on measurement of ethanol in the broth. Now the I-part of conventioanl PID-control is replaced with an observer of of the culture growth rate. In this way the ethanol set-point can be kept.

* BPL\_CHO\_Perfusion\_bleed\_control - The setup shows perfusion control where the bleed stream is controlled based on measurent of viability of the culture. A technique often used. 

* BPL\_CHO\_Batch\_qP\_calibration - In this example we illustrate the possilibitie to calibrate the function of recombinant protein expression $q_P()$  given that the model of cell growth and metabolism is known. Both a traditional model of $q_P()$ as a linear function with saturation, as well as a more flexible neural network model, are tested on simulated data. 


**Note 2025-mm-yy** 

Here is a new repository including control design of fedbatch cultivation, made on request.
The example is about feed rate control of yeast cultivation during fedbatch with focus on 
how to address variations in the culture exponential growth rate. The analysis and the design is applicable
to control of other variables during fedbatch, like dissolved oxygen, pH etc. 

* An example of fedbatch cultivation of yeast with control of the ethanol concentration - see repository BPL\_YEAST\_Fedbatch\_control
