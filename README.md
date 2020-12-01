# Realsense-ros-gazebo

This repository contains all the code required to use both the simulated and real RealSense cameras with ROS. The simulated camera is implemented in [Gazebo](https://wiki.ros.org/gazebo).

## Implemented cameras

It currently contains the gazebo implementation for the:

-   Realsense D335
-   Realsense D435i

Feel free to add a pull_request/issue might you need support for any of the other cameras.

## How to use

### Installed the dependencies

In order to use this package you first have to make sure you installed the required Realsense libraries. A guide on how this is done can be found in [the realsense documentation](https://www.intelrealsense.com/get-started/).

### Build the package

As this repository contains submodules you have to clone it recursively:

```bash
git clone --recurse-submodules
```

### Use the package

To see the package in action source the catkin `./devel/setup.bash` script. A example can then be started using the following command:

```bash
roslaunch realsense2_description view_d435_model_rviz_gazebo.launch
```

## Acknowledgement

This repository was created following the guide on the [realsense2_description]\(<https://github.com/issaiass/realsense2_description> repository of [@issaiass](https://github.com/issaiass)
