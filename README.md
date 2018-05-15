# Skeleton-Code
Code for interpreting skeleton data for activity recognition

Three different representations are implemented - Relative Distances and Angles of Star Skeleton(RAD), Histogram of Joint Position Differences (HJPD), Histogram of Oriented Displacements(HOD)

Compiling the code - 

The c++ code can be compiled by using the linux g++compiler for linux.
Open a new command window.
change directory to Skeleton_code
run the command " g++ -std=c++11 HOD.cpp" to run HOD code.
To check the output" ./a.out"
run the command " g++ -std=c++11 RAD.cpp" to run RAD code.
To check the output" ./a.out"
run the command " g++ -std=c++11 HJPD.cpp" to run HJPD code.
To check the output" ./a.out"

The output vectors are stored in

RAD

TEST rad_h1.t
TRAIN rad_h1

HJPD

TEST hjpd_h1.t
TRAIN hjpd_h1

HOD

TEST hod_h1.t
TRAIN hod_h1

For the RAD configuration

The joints are taken as 
//centre = 1
//head = 4
//larm = 8
//rarm = 12
//lleg = 16
//rleg = 20
The distances and angles are calculated from the first joint to the others.
The bin sizes are taken as 10 for both angle and distance histograms.
The code contains lines for implementing the training and test sets seperately. Uncommenting and commenting give both files.
Vector length = 5*(M+N) = 5*(10+10) = 100

For the HJPD configuration

All the joints are taken into a factor and relative distances from the base joint (1) are calculated. The histogram bin size is taken as 5.The code contains lines for implementing the training and test sets seperately. Uncommenting and commenting give both files.

For the HOD configuration

Every joint is taken into consideration for the weighted histogram representation. Instead of adding one for the frequency the distance weight is added to the histogram 

