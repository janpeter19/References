# Notes history

**Note 2025-02-07**
Now the issue with running notebooks with PyFMI is resolved and running latest version 2.16.3. 

**Note 2025-01-25**
Please use notebooks using FMPy instead of PyFMI. 
There is an installation problem with the notebooks using PyFMI and reported and got issue number
[#287.](https://github.com/modelon-community/PyFMI/issues/287) 
      
**Note 2024-11-11** 
The BPL is updated to ver 2.3.0 and now used in all examples. The GUI part has been developed in parallell with the main development of the library for more than a year. Now it is fully integrated and this update is an important consolidating step. Focus has been to use standard Modelica GUI facilities and to simplify the code. The main structure of the code still follows well the outline in section 6 in the paper referred above. The library has been tested mainly with the GUI of OpenModelica and Modelon Impact.

**Note 2024-10-04**
The GUI for BPL ver 2.2.1 is an update with minor adjustments after now longer of time usage.

Further, the possibility to simulate, change a parameter, and then continue simulation using the command simu('cont'), now finally works also for OpenModelica Linux FMUs, see their Github-list of issues #12561.  The command is part of the simplified interface FMU-explore for the packages PyFMI and FMPy. 

OpenModelica nightly build 1.25.0-dev after 2024-10-02 is now used throughout for running notebooks in Google Colab.

**Note 2024-07-20**
The GUI for BPL has now reached an important milestone and all applications can be GUI-configured and the notebooks include corresponding process diagram. The models and results are the same, of course. Recent GUI work:

* An example of fedbatch cultivation of yeast with control of dissolved oxygen (now also including icons for the gasphase) - see repository BPL\_YEAST\_AIR\_Fedbatch

* An example of ion exchange chromotagraphy - see repositories BPL\_IEC\_validation (but BPL\_IEC\_operation needs a fix around scale_volume, i.e. scaling of the time axis).

OpenModelica 1.23.1 was used. In the fall a subset of GUI for the liquid phase only was validated with Impact 2.1 

The issue #12561 with the OpenModelica FMUs still remains / fixed nighly build 1.25.0-dev 2024-10-02.

**Note 2024-07-04**
The BPL is updated to 2.2.1 and the GUI for gasphase is included, see the process diagram for BPL\_YEAST\_AIR Fedbatch DO-control. In general, the gasphase is coloured in grey, while liquid media is as before for nutriens yellow, for cells orange, and for recombinant product violet. The simulation results are identical and the underlying model code only differs in a few variable names. Text material like UsersGuide with References in MSL-style are now also included. Here is an old subtle problem with the FMUs that occurs when simulations are re-started at some point. It has nothing to do with update of BPL. The OpenModelica community works on it, see issue #12561 on their GitHub-site. 

Note that Google Colab automatically introduce a code line at the end "Start coding or generate with AI" as some kind of advertisment. It is difficult to take away.

**Note 2024-05-24**
Now PyFMI 2.13.0 is available again, as well as FMPy 0.3.20, for running the simulations in the notebooks.
Now Linux FMUs are updated to OpenModelica ver 1.23.0-dev. The FMUs are compiled with recently updated Bioprocess Library 2.2.0. The common command-line interactions for both PyFMI and FMPy is done with FMU-explore updated to 1.0.0. 

**Note 2024-05-22**
Here is a problem with PyFMI 2.13-0 installation using conda-forge and seems not possible to go back to the earlier version either. The problem is reported to the people in charge. In the mean time, use FMPy that works fine. Now Linux FMUs are updated to OpenModelica ver 1.23.0-dev. The FMUs are compiled with recently updated Bioprocess Library 2.2.0.

**Note 2024-05-06**
Now the simulations are run with latest Python package PyFMI 2.12-0, or alternatively FMPy 0.3.20.
It seems to work well but let me know if you encounter any problems.

**Note 2024-01-18**
The conference paper "Design ideas behind Bioprocess Library for Modelica" by myself, and presented at the 15th International Modelica Conference in the fall, you can now find in the proceeding [here](https://ecp.ep.liu.se/index.php/modelica/issue/view/83) on page 453-462.

  **CONF\_2023\_10\_MODELICA15**  - The repository contains  a few basic examples used for illustrations in the paper.
  
**Note 2023-10-04**
The BPL ver 2.1.1 with GUI-configured applications with only liquidphase passed validation successfully with Modelon Impact Cloud ver 2.9.25 for Windows. 

**Note 2023-09-26**
I would like to draw your attention to two conference contributions recently and examples represented in the repositories. Here will be some further updates in the coming days.

  **CONF\_2023\_08\_NPCW24** - The example on ion chromatography was presented that we have worked on for some time.

  **CONF\_2023\_10\_MODELICA15**  - The design ideas behind BPL is presented with focus on the library structure. A few basic examples are used for illustration and found here.

  Now PyFMI works as usual again after adjustments in the package environment. And you also alternatively can use FMPy as before.

**Note 2023-09-13**
Now several notebooks also include a process diagram. They are generated from GUI configuration using OpenModelica and BPL equipped with icons. This new version of BPL with GUI is under further development. I am also aware of that notebooks with PyFMI do halt for some errors in the package environment. In the meantime, use notebooks with FMPy instead and available in most repositories. 

**Note 2023-08-15** The Google Colab VM has recently been updated to Ubuntu 22.04 and runs Python 3.10 and enables us to use the latest version of the key package PyFMI. Most FMUs are still made for Ubuntu 20.04 but still works what I can see after testing a few notebooks.

**Note 2023-03-30** Now the setup scripts including FMU-explore ver 0.9.7 has after a longer trial period matured and provide interface for both the packages PyFMI and FMPy and almost identical notebooks can be used. The  different setup scripts for both packages  have very similar structure.  The difficulties to load PyFMI is now eliminated and was due to mismatch between Colab and Miniconda.   Colab now use Python 3.9 as default. Here are several new repositories in the pipe-line. Stay tuned!

**2023-03-22** There is still a problem with Google Colab VM and PyFMI.  However,  now I have added a link to almost all notebooks for using FMPy instead to run the FMUs. This is still experimental and further improvements will be done in the setup-scripts. 

**2023-03-16** The Google Colab VM has for a week problem with the package PyFMI. You can look at the PDF of the notebooks though. For the repository BPL_TEST2_Batch_calibration the notebook can be run with the alternative package that is for evaluation.

**2023-02-20** 
The Google Colab VM has in mid January been updated to Ubuntu 20.04 and runs now Python 3.8 and enables us to use the latest version of the key package PyFMI.  This is all good news! The software has been updated accordingly.

**2023-01-16**
The Google Colab VM updated from Ubuntu 18.04 LTS (Python 3.7 default) to Ubuntu 20.04 LTS (Python 3.8 default). 
This means updates are needed in the different repositories concerning scripts and re-compilation of FMUs to function.
