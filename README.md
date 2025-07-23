# SHDynamicsNotebooks
Andrew R. Axelsen, 2025

This code may be used for the purposes of conducting research, but credit must be given.

---

# ABOUT

This is the collection of Jupyter Notebooks used for the research papers: "Hyperbolicity and Southern Hemisphere Persistent Synoptic Events" and "Covariations between persistent synoptic features and Antarctic sea ice via unsupervised regression learning."

This collection of notebooks requires code from the following project in order to be used: https://doi.org/10.5281/zenodo.4035644

After downloading the code, you will need to perform several other tasks to make the code work:

-Download the datasets: We use the NCEP/NCAR Reanalysis datasets, these datasets are available in yearly chunks and will need to be concatenated manually using ncrcat or an equivalent script. For alternative datasets, adjustments will be required to make work, an example of this is in SH-EventsAnalysis.ipynb, where we convert stereographic projections into lat-lon format (code from https://github.com/nsidc/polarstereo-lonlat-convert-py).

-Generate the FEM-BV-VAR Models: Use the code in the linked Zenodo code and use the given shell scripts. Note that the code given is optimised for use on the Gadi supercomputer, and may require adjustments to use with other supercomputers or locally.

Extra for "Hyperbolicity and Southern Hemisphere Persistent Synoptic Events":

-Generate the CLVs: You will need to use the appropriate CLV file from the linked Zenodo code (calculate_CLVs.py). You may also wish to create a shell script to call the relevant Python files.

The linked code was used for the project: "Dynamical analysis of a reduced model for the North Atlantic Oscillation." We thank the authors of this paper for creating the code used in these studies.

---

# FILES
AnomFile_Concatenator.ipynb - This routine allows one to concatenate anomaly files of different variables and levels into one, as well as a regridding routine if required

produce_eofs_Multivar.ipynb - Similar to produce_eofs.ipynb from the required FEM-BV-VAR_dynamics-master project, but handles multivariate cases as well as multi-level cases.

SH-Dynamics-Notebook.ipynb - Main notebook used for the paper: "Hyperbolicity and Southern Hemisphere Persistent Synoptic Events." Covers the various routines, manual adjustments will be required to make work.

SH-EventsAnalysis.ipynb - Main notebook used for the manuscript: "Covariations between persistent synoptic features and Antarctic sea ice via unsupervised regression learning." Covers the various routines, manual adjustments will be required to make work.
