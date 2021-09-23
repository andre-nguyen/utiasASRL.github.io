---
permalink: /vtr3/
title: "Visual Teach & Repeat 3"
# excerpt: "About me"
author_profile: true
redirect_from: 
    # - /vtr3/
#   - /about/
#   - /about.html
---
This is the website for the Visual Teach and Repeat 3 (VT&R3) package, which is the C++ implemenation of the Visual Teach and Repeat system for robot navigation with a camera or LiDAR sensor. The package is developed and maintained by the Autonomous Space Robotics Lab (ASRL) at the University of Toronto Institute for Aerospace Studies (UTIAS). 


# Description

Visual Teach and Repeat (VT&R) is a navigation system for mobile robots. In the teach phase, a user drives the robot manually to teach a path, while the system builds a map. Afterwards, during the repeat phase, the map is used for localization as the robot follows the path autonomously. VT&R relies on local submaps only, which facilitates repetition of long paths without the need for accurate global reconstruction. 

VT&R handles long-term navigation with the use of multi-experience localization. Each time the robot repeats a path, data from this new experience is stored in the spatio-temporal pose graph. Previously collected experiences can then be used to bridge the appearance gap for localization to the map as the environment changes.

VT&R3 is a C++ implementation of Visual Teach and Repeat. It is designed for easy adaptation to various robots and sensors, such as camera, LiDAR, RaDAR, or GPS. The current implementation includes a feature-based pipeline that uses a stereo camera, as well as a point-cloud-based pipeline for LiDAR sensors. More detailed description of VT&R3 can be found in this [wiki page](https://github.com/utiasASRL/vtr3/wiki/Introduction-to-VTR3).


<iframe width="560" height="315" src="https://www.youtube.com/embed/udI328uO7Qg?start=14" frameborder="0" allowfullscreen></iframe>


<b></b>


# Hardware Requirements
To run VT&R3, you will need the following hardware:
- A ROS enabled robot platform. VT&R3 has been thoroughly tested on the Clearpath Grizzly robot.
- A NVIDIA GPU-enabled machine that can run Ubuntu 20.04. We have tested on the following laptop models: 
  - [Lenovo Notebook ThinkPad P53](https://www.lenovo.com/ca/en/laptops/thinkpad/thinkpad-p/P53/p/22WS2WPWP53)
  - [Lenovo Notebook ThinkPad T15g Gen2](https://www.lenovo.com/ca/en/laptops/thinkpad/thinkpad-t-series/ThinkPad-T15g-Gen-2-15-inch-Intel/p/WMD00000484)

You would also need the following stereo camera or spinning LiDAR. 
- [Bumblebee XB3 Stereo Camera](https://www.flir.ca/support/products/bumblebee-xb3-firewire/#Overview)
- LiDAR: Waymo Honeycomb, [Velogyne Alpha Prime](https://velodynelidar.com/products/alpha-prime/). 

For more information, please refer to the Installation Guide under [Hardware Recommendation](https://github.com/utiasASRL/vtr3/wiki/Installation-Guide). We are actively working towards enabling supports for more sensors. More info on that will be updated on this [wiki page](https://github.com/utiasASRL/vtr3/wiki/Setting-Up-VTR3-with-a-New-Sensor-or-Robot). 



# Installation
<!-- ====== -->
Please follow the [Installation Guide](https://github.com/utiasASRL/vtr3/wiki/Installation-Guide) to install VT&R3 and its dependencies. 


# Demonstration for Online VT&R3
<!-- ====== -->
Please see the following tutorial on how to run VT&R3 online on Grizzly robot. This tutorial gives basic info on how to use the UI to teach and repeat a path. More info on how to launch VT&R3 can be found on this [Wiki page](https://github.com/utiasASRL/vtr3/wiki/Installation-Guide). 
(insert Jordy's video here)
<iframe width="560" height="315" src="https://www.youtube.com/embed/qM8b89Jftv4" frameborder="0" allowfullscreen></iframe>

<b></b>


# Extension Plan
Below is a list of features that we are currently working on. If you have encountered any other issues while running VT&R3, feel free to create a new issue on our [GitHub page](https://github.com/utiasASRL/vtr3/issues). If you have any specific feature request, please directly contact us at vtr@robotics.utias.utoronto.ca. 

## Path-Tracker Overhaul
In recent testing we have noticed some sub-optimal path tracking behavior under niche conditions. We will not be addressing these individual bugs immediately as in the near future we will be re-writing the current path tracker to implement constrained model predictive control associated with upcoming research.

## RaDAR VT&R
We are working on enabling RaDAR-based localization in VT&R in the upcoming release. 

## Support for ZED Stereo Camera
We are currently working towards enabling support for ZED stereo camera in our VT&R framework. More detailed instructions on how to set up ZED camera and other sensors will be added to this [wiki page](https://github.com/utiasASRL/vtr3/wiki/Setting-Up-VTR3-with-a-New-Sensor-or-Robot). 

# Gallery of Robots that Use VT&R
Below are all the robots that use our framework. 

<img width="660" height="515" src="../images/collaborators.png">



# Related Work
<!-- ====== -->
[1] Furgale P T and Barfoot T D. “Visual Teach and Repeat for Long-Range Rover Autonomy”. Journal of Field Robotics, special issue on “Visual mapping and navigation outdoors”, 27(5):534–560, 2010. doi: [10.1002/rob.20342](https://onlinelibrary.wiley.com/doi/10.1002/rob.20342), ([google](https://scholar.google.ca/scholar?q=10.1002/rob.20342)). ([pdf](http://asrl.utias.utoronto.ca/~tdb/sbib/furgale_jfr10.pdf)), ([video1](http://www.youtube.com/watch?v=KW8vi0791JI)), ([video2](http://www.youtube.com/watch?v=gwe6pFtxp5w)), ([video3](http://www.youtube.com/watch?v=5bcKwrL_1As))

    @article{Furgale2010VisualTA,
    title={Visual teach and repeat for long-range rover autonomy},
    author={P. Furgale and T. Barfoot},
    journal={J. Field Robotics},
    year={2010},
    volume={27},
    pages={534-560}
    }

[2] Paton M, MacTavish K A, Warren M, and Barfoot T D. “Bridging the Appearance Gap: Multi-Experience Localization for Long-Term Visual Teach and Repeat”. In Proceedings of the IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS), pages 1918–1925. Daejeon, Korea, 9-14 October 2016. doi: [10.1109/IROS.2016.7759303](https://ieeexplore.ieee.org/document/7759303), [(google)](https://scholar.google.ca/scholar?q=10.1109/IROS.2016.7759303)

    @article{Paton2016BridgingTA,
      title={Bridging the appearance gap: Multi-experience localization for long-term visual teach and repeat},
      author={M. Paton and K. MacTavish and M. Warren and T. Barfoot},
      journal={2016 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)},
      year={2016},
      pages={1918-1925}
    }

