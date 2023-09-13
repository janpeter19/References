# Notes history
**Note 2023-06-01** Now the setup scripts using PyFMI works again. They have been updated for Python 3.10 that is now default version for Colab VM since a few weeks. The scripts for FMPy are more robust. Further here are a few new repositories with preliminary notebooks:
    
* BPL_YEAST_COB_Batch - illustrate constraint-based modelling and simulation with FMU and Optlang in combination.
* BPL_IEC_operation - show downstream ion exchange chromatography in operation in several typical situations 
* BPL_IEC_validation - show downstrean ion exchange chromatograph show similarity with original work

**Note 2023-08-15** The Google Colab VM has recently been updated to Ubuntu 22.04 and runs Python 3.10 and enables us to use the latest version of the key package PyFMI. Most FMUs are still made for Ubuntu 20.04 but still works what I can see after testing a few notebooks.

**Note 2023-03-30** Now the setup scripts including FMU-explore ver 0.9.7 has after a longer trial period matured and provide interface for both the packages PyFMI and FMPy and almost identical notebooks can be used. The  different setup scripts for both packages  have very similar structure.  The difficulties to load PyFMI is now eliminated and was due to mismatch between Colab and Miniconda.   Colab now use Python 3.9 as default. Here are several new repositories in the pipe-line. Stay tuned!

**2023-03-22** There is still a problem with Google Colab VM and PyFMI.  However,  now I have added a link to almost all notebooks for using FMPy instead to run the FMUs. This is still experimental and further improvements will be done in the setup-scripts. 

**2023-03-16** The Google Colab VM has for a week problem with the package PyFMI. You can look at the PDF of the notebooks though. For the repository BPL_TEST2_Batch_calibration the notebook can be run with the alternative package that is for evaluation.

**2023-02-20** 
The Google Colab VM has in mid January been updated to Ubuntu 20.04 and runs now Python 3.8 and enables us to use the latest version of the key package PyFMI.  This is all good news! The software has been updated accordingly.

**2023-01-16**
The Google Colab VM updated from Ubuntu 18.04 LTS (Python 3.7 default) to Ubuntu 20.04 LTS (Python 3.8 default). 
This means updates are needed in the different repositories concerning scripts and re-compilation of FMUs to function.
