# FastLoc
A fast machine learning based algorithm for determination of local earthquakes location.

# Required Softwares:
Nothing !

# Description of files

1- Grids.dat
------------

Grid points within the area of interest supposed to be learnt by the trainer. This file will be built by the program.


2- Area_Vel
------------

This file contains the velocity model used by the trainer to work on the grid points. This is used to build a proper formatted velocity model (Velmodel.tvel).

You can rename this file, but then you must chnage the line 12 in Synthetic_Trainer.

Define your velocity model in the following format (do not remove the header line!).

Depth(km)  Vp(km/s)  Vs(km/s)  


3- stations.info
-----------------

A file containing spatial coordinates of all available stations within the area of interest.

Format must be as follows:

Name Latitude(deg) Longitude(deg)

4- stations.used
----------------

This file contains a list of stations which user desires to be used during the whole process. You might have 100 stations in your area of interest (defined in stations.info) but remember that all processes (e.g. training and event detection) will be done only using these stations. You are NOT allowed to alter this file once you trained your region.

For a better result, it is recommended to provide the P arrivals in the input for all the stations defined in this file. Input files must be located in the Input/ directory, in .dat files and in the following format (look at examples):

station_name First_P_arrival(hh:mm:ss.ms)

KCHF 20:26:01.9

GLG1 20:26:06.3

5- sta_sta_dist
--------------

This file contains the distance between each couple of stations (station1, station2). You will be asked to whether update this file or not every time you run the Synthetic_Trainer.

# ~~~~~ How to use this Program? ~~~~~~

First of all you need to prepare the following requisites:

1- consider a region of interest and define it in the Synthetic_Trainer file, lines 13-15.

2- Prepare a velocity model as explaiend above and set its name in the Synthetic_Trainer file, line 12.

3- Define the desired station names in the stations.used file.

4- run the trainer.

5- Once the trainer did its job (you will have a set of database in Database/ directory) you can test the program (Locate) by providing some input files.

Feel free to contact me in case of any errors.
----------------------------------------
















