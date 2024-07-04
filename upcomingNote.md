**Note 2024-07-04
The BPL is updated tp 2.2.1 and the GUI for gasphase is included, see the process diagram for BPL\_YEAST\_AIR Fedbatch DO-control. The gasphase is coloured in grey, while liquid media is as before for nutriens yellow, for cells orange, and for recombinant product violet. The simulation results are identical and the underlying model code only differs in a few variable names. Text material like UsersGuide with References in MSL-style are now also included. Here is a subtle problem with the FMUs that occurs when simulations are re-started at some point and the OpenModelica community works on it, see issue #12561 on their GitHub-site.

Note, Google Colab automatically introduce a code line at the end "Start coding or generate with AI" as some kind of advertisment. It is difficult to take away.


**Note 2024-05-xx**
The BPL is updated to 2.2.0. The names of initial values are changed to using the suffix "start" to comply with the Modelica Standard Library practice. Some other parameter names are also modified. Therefore FMUs are recompiled, Python setup files are updated, and also notebooks. Due to changes in the Google Colab framework, printed notebooks get truncated and for the time being just accept that. See Stackoverflow 
[post](https://stackoverflow.com/questions/77860909/how-to-avoid-truncation-of-jupyter-notebooks-printed-from-colab-using-chrome)

The BPL applications are compiled OpenModelica 1.22.2 (Linux) amd with (depracated) JModelica 2.14 (Windows). 
In the fall 2023 the compliance with Impact from Modelon was validated. 

The conference paper "Design ideas behind Bioprocess Library for Modelica" by myself, and presented at the 15th International Modelica Conference in 2023, you can now find in the proceeding  [here](https://ecp.ep.liu.se/index.php/modelica/issue/view/83) on page 453-462.

Direct to the paper
[here](https://ecp.ep.liu.se/index.php/modelica/article/view/955) 


Earlier notes you find 
[here](https://github.com/janpeter19/References/blob/main/Notes.md).


