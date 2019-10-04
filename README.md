# RDC2018
Package for the ROS Developer Conference 2018

Usage:
------
After the installation, open a terminal to run the ```roscore```.
In anotherterminal launch:

```roslaunch RDC2018 cartesio.launch```

then in the third terminal run ```rviz```.
In the ```Displays``` window of RVIZ, set the ```Fixed Frame``` under ```Global Options``` to ```ci/world_odom```. 

Now add a ```RobotModel``` and set as ```TF Prefix```: ```ci```, you should now see the robot in RVIZ. 

Finally add an ```Interactive Marker``` to control the end effector. The interactive marker topic lists all the available end-effectors (from the stack file). To enable the control right click on the marker and select ```Continuous Control```.

To control the postural null-space of the robot, in another terminal run:

```rosrun cartesian_interface postural_gui```.
