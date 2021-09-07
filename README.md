# CppND-L2-Project

This project is the first step in final project for the Concurrency Part of the Udacity C++ Nanodegree. This is a concurrent traffic simulation and the purpose is to simulate traffic in a city grid with vehicles, streets and intersections. Vehicles drive around randomly and change direction at each intersectoin. Each object in the city grid will run independently in its own thread.

The task is to understand the code base and complete where needed to get this first running version of traffic simulation.

## Code Overview

<img src="data/Screenshot from 2021-09-07 13-21-48.png" > 


## Project Tasks

* Task L2.1 : In method Vehicle::drive(), start up a task using std::async which takes a reference to the method Intersection::addVehicleToQueue, the object _currDestination and a shared pointer to this using the get_shared_this() function. Then, wait for the data to be available before proceeding to slow down.
* Task L2.2 : In method Intersection::addVehicleToQueue(), add the new vehicle to the waiting line by creating a promise, a corresponding future and then adding both to _waitingVehicles. Then wait until the vehicle has been granted entry.
* Task L2.3 : In method WaitingVehicles::permitEntryToFirstInQueue(), get the entries from the front of _promises and _vehicles. Then, fulfill promise and send signal back that permission to enter has been granted. Finally, remove the front elements from both queues.


## Dependencies

* cmake>=2.8
* make >= 4.1 (Linux, Mac), 3.81 (Windows) 
* OpenCV >= 4.1
* gcc/g++ >= 5.4

## Build Instructions

1. Clone this repository
2. Make a build directory: mkdir build && cd build
3. Compile: cmake .. && make
4. Execute: ./traffic_simulation.


