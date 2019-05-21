# MOM6-Hurricane

This repository provides configurations (input parameters and data) of MOM6 for
simulating the ocean response to tropical cyclones in forced simulations.

# Directory Tree

The top level directory structure groups the source code and input files as follow:

| File/directory              | Purpose |
| --------------              | ------- |
| ```README.md```             | this file with basic pointers to more information. |
| ```src/```                  | source code for MOM6, SIS2 and FMS-shared code. |
| ```ice_ocean_SIS2```        | experiments that use MOM6 and SIS2 code in coupled mode |

| Directory            | Purpose |
| ---------            | ------- |
| ```src/MOM6/```      | is a git submodule that contains the source code for MOM6 |
| ```src/SIS2/```      | is a git submodule that contains the source code for SIS2 |
| ```src/FMS/```       | is a git submodule that contains the source code for FMS |

# Build Instructions

To build the source coded stored in the 'src' directory, please see the descriptions here:
(https://github.com/NOAA-GFDL/MOM6-examples/wiki), but note that the instructions for 
obtaining the '.datasets' folder are different for this repository than in the primary
NOAA-GFDL/MOM6-examples repository.  See the section below for more details on obtaining
and setting up the .datasets.

MOM6 can be built in several modes depending on the coupled configurations needed for the
example case desired.  This repository will specifically support either ocean_only mode 
(not yet supported by present examples within this repository, but will be supported by 
future 'ocean_only' examples) and ice_ocean_SIS2 mode.  The resulting executables can be 
used to conduct the experiments in the corresponding example folders.

# Sample Cases

At present there is 1 sample case included:
-ice_ocean_SIS2/WestPacific,
which is modeled after ice-ocean coupled experiments in the original MOM6 repository 
(https://github.com/NOAA-GFDL/MOM6-examples).  Samples within ice_ocean_SIS2 rely
on first building the ice_ocean_SIS2 executable:
 (https://github.com/NOAA-GFDL/MOM6-examples/wiki/Getting-started#compiling-mom6-in-mom6-sis2-coupled-mode)
Multiple sub-cases will be included within the WestPacific directory, varying ocean settings such as 
horizontal resolution.

# Datasets

The examples included here rely on a unique '.datasets' folder compared to the primary
MOM6-examples repository.  A link will eventually be included here, but for now the repository
administrators will provide the data on an 'as-needed' basis.  The datasets folder obtained
Will need to be included at the top-level (e.g., MOM6-Hurricane) in a folder named '.datasets',
where relative symlinks are relied upon to propagate the data to the appropriate example folders.