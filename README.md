# Extended Kalman Filter Project Starter Code
Self-Driving Car Engineer Nanodegree Program

In this project I utilize a kalman filter to estimate the state of a moving object of interest with noisy lidar and radar measurements.

[XCode]: ./data/Xcode.png  "XCode image"
[simulator]: ./data/screenshot.png  "simulator image"

This project involves the Term 2 Simulator which can be downloaded [here](https://github.com/udacity/self-driving-car-sim/releases)


Once the install for uWebSocketIO is complete, the main program can be built and run by doing the following from the project top directory.


Note that the programs includes src/FusionEKF.cpp, src/FusionEKF.h, kalman_filter.cpp, kalman_filter.h, tools.cpp, and tools.h

The program main.cpp has already been filled out by the project, except added some "cout", I dit not modify it.

main.cpp is using uWebSocketIO, which listen incoming message from the simulator, do some processing with EKL algorithms, then sent back to the simulator.

# Message samples
Bellow are the samples of the messages processed and transmitted on uWebSocketIO protocol.

## Incoming messages
### Radar message

    ["telemetry",{"sensor_measurement":"R 6.673922e+00 1.256145e-01 5.006870e+00 1477010444150000 6.561105e+00 7.925232e-01 5.141571e+00 4.883049e-01 9.468793e-02 1.633729e-01"}]

### Lidar message

    ["telemetry",{"sensor_measurement":"L 6.782143e+00 7.140359e-01 1477010444200000 6.818081e+00 8.179882e-01 5.134523e+00 5.299897e-01 1.028566e-01 1.699593e-01"}]

## Outgoing messages

    42["estimate_marker",{"estimate_x":6.57681376720585,"estimate_y":0.744203439825412,"rmse_vx":1.53157158633846,"rmse_vy":0.899409160527193,"rmse_x":0.130520370666516,"rmse_y":0.0706979550892104}]


## Running OUTPUT

Final RMSE output as Bellow

    42["estimate_marker",{"estimate_x":-7.23245983073131,"estimate_y":10.8959188865611,"rmse_vx":0.451266739945118,"rmse_vy":0.43993508070814,"rmse_x":0.097317778752952,"rmse_y":0.0854597168623381}]

The simulator screenshot as bellow:

  ![simulator][simulator]

  The RMS output meets the requirements which is as bellow

    px, py, vx, vy output coordinates must have an RMSE <= [.11, .11, 0.52, 0.52]

# Program IDE setup and Build

## build
  1. mkdir build
  2. cd build
  3. cmake ..
  4. make
  5. ./ExtendedKF

  I use XCode as develop environment, more details about how to setup is referred from bellow link
   [here](https://github.com/udacity/CarND-Extended-Kalman-Filter-Project/tree/master/ide_profiles/xcode)

## Screenshot of the XCode IDE

![XCode][XCode]
