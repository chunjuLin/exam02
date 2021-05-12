# exam02

First of all we have to record the data from the accelerator. For the one that we have to find the gesture mode 
is pretty similar to the original mbed08. We use the ML to juged what is the gesture we have done. However, we still 
have to see if the data is over the angle. First of all, at the begin of the main.  I collected the horizontal data.
After collecting the horizontal data, we start multiple thread to do each job such as find the gesture and feature.
If we key in the rpc function as /capture/run 1. It will start the ML function to find the gesture. Also, we have to 
open a thread for the feature, it will continue with the time. When a gesture is determined, we will send a message from
mqtt to the python as (more_th , gesture). We use the python to anaylsis each data, and save in each array. If we got ten 
data, the python will print out the result.  
