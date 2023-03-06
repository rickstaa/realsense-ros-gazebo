# Realsense-ros-gazebo

[![Codacy Badge](https://app.codacy.com/project/badge/Grade/af9c95b115fc49499bbc058f22cd4adf)](https://www.codacy.com/gh/rickstaa/realsense-ros-gazebo/dashboard?utm_source=github.com&utm_medium=referral&utm_content=rickstaa/realsense-ros-gazebo&utm_campaign=Badge_Grade)
[![GitHub release (latest by date)](https://img.shields.io/github/v/release/rickstaa/realsense-ros-gazebo)](https://github.com/rickstaa/realsense-ros-gazebo/releases)
[![ROS versions](https://img.shields.io/badge/ROS%20versions-melodic%20%7C%20noetic-brightgreen)](https://wiki.ros.org)
[![Contributions](https://img.shields.io/badge/contributions-welcome-orange.svg)](contributing.md)

This repository contains all the code required to use both the simulated and real RealSense cameras with ROS. The simulated camera is implemented in [Gazebo](https://wiki.ros.org/gazebo). It contains the following submodules:

-   [realsense_gazebo_plugin](https://github.com/rickstaa/realsense_gazebo_plugin/tree/melodic-devel)
-   [realsense-ros](https://github.com/rickstaa/realsense-ros/tree/development-gazebo)

## Implemented cameras

It currently contains the gazebo implementation for the:

-   [Realsense D335](https://github.com/rickstaa/realsense-ros/blob/development-gazebo/realsense2_description/launch/view_d435_model_rviz_gazebo.launch)
-   [Realsense D435i](https://github.com/rickstaa/realsense-ros/blob/development-gazebo/realsense2_description/launch/view_d435i_model_rviz_gazebo.launch)

Feel free to add a [pull_request/issue](https://github.com/rickstaa/realsense-ros-gazebo/issues) might you need support for any of the other cameras.

## How to use

### Installed the dependencies

To use this package, you first have to make sure you installed the required Realsense libraries. A guide on how this is done can be found in [the realsense documentation](https://www.intelrealsense.com/get-started/). Additionally you also have to make sure [ROS](https://wiki.ros.org/ROS/Installation) and [Gazebo](https://wiki.ros.org/gazebo) are installed.

### Build the package

In order to build the package you have to create a catkin workspace. You can then clone the repository in the src folder using the following command:

```bash
mkdir ~/catkin_ws
cd ~/catkin_ws
git clone --recurse-submodules https://github.com/rickstaa/realsense-ros-gazebo.git src
```

Please make sure you use the `--recursive-submodules` flag as this repository contains submodules. After you cloned the repository you can install the ros dependencies using the following command:

```bash
rosdep install --from-paths src --ignore-src --rosdistro melodic
```

When this is done you can build the package using one of the following commands:

```bash
catkin_make
```

```bash
catkin build
```

### Use the package

To see the package in action source the catkin `./devel/setup.bash` script. An example can then be started using the following command:

```bash
roslaunch realsense2_description view_d435_model_rviz_gazebo.launch
```

## Acknowledgement

This repository was created following the guide on the [realsense2_description](https://github.com/issaiass/realsense2_description) repository of [@issaiass](https://github.com/issaiass)

## Contributing

Feel free to open an issue if you have ideas on how to make this GitHub action better or if you want to report a bug! All contributions are welcome. :rocket: Please consult the [contribution guidelines](CONTRIBUTING.md) for more information.
