---
permalink: / #vtr3/ #test remove this?
title: "Visual Teach & Repeat 3"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
  # - /vtr3/ 
---

<!-- <iframe width="300" height="200" src="VTR3_Argo.mp4" type="video/mp4"></iframe> -->

<!-- <video id="example_video_1" class="video-js vjs-default-skin" width="640" height="264" src="VTR3_Argo.mp4" type='video/mp4' />
</video> -->

This is the website for the Visual Teach and Repeat 3 (VT&R3) package, which is the software implemenation of the Visual Teach and Repeat system for robot navigation with a camera or LiDAR sensor. The package is developed and maintained by the Autonomous Space Robotics Lab (ASRL) at University of Toronto Institute for Aerospace Studies. 

<!-- This is the front page of a website that is powered by the [academicpages template](https://github.com/academicpages/academicpages.github.io) and hosted on GitHub pages. [GitHub pages](https://pages.github.com) is a free service in which websites are built and hosted from code and data stored in a GitHub repository, automatically updating when a new commit is made to the respository. This template was forked from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/) created by Michael Rose, and then extended to support the kinds of content that academics have: publications, talks, teaching, a portfolio, blog posts, and a dynamically-generated CV. You can fork [this repository](https://github.com/academicpages/academicpages.github.io) right now, modify the configuration and markdown files, add your own PDFs and other content, and have your own site for free, with no ads! An older version of this template powers my own personal website at [stuartgeiger.com](http://stuartgeiger.com), which uses [this Github repository](https://github.com/staeiou/staeiou.github.io). -->
<!-- 
Table of Content
======

- [Discription](#description)
- [Hardware](#hardware)
- [Demo](#demo)
- [Installation](#installation)
- [Related Work](#related-work)
 -->

# Description

Visual Teach and Repeat (VT&R) is a navigation system for mobile robots. In the teach phase, a user drives the robot manually to teach a path, while the system builds a map. Afterwards, during the repeat phase, the map is used for localization as the robot follows the path autonomously. VT&R relies on local submaps only, which facilitates repetition of long paths without the need for accurate global reconstruction. 

VT&R handles long-term navigation with the use of multi-experience localization. Each time the robot repeats a path, data from this new experience is stored in the spatio-temporal pose graph. Previously collected experiences can then be used to bridge the appearance gap for localization to the map as the environment changes.

VT&R3 is the C++ implementation of Visual Teach and Repeat. It is designed for easy adaptation to various robots and sensors, such as camera, LiDAR, RaDAR, or GPS. The current implementation includes a feature-based pipeline that uses a stereo camera, as well as a point-cloud-based pipeline for LiDAR sensors.

<!-- https://youtu.be/udI328uO7Qg -->

<iframe width="560" height="315" src="https://www.youtube.com/embed/udI328uO7Qg?start=14" frameborder="0" allowfullscreen></iframe>
text...



# Hardware Requirements
To run VT&R 3, you need the following hardware:
- ROS2 enabled robot platform. VT&R 3 has been tested on the following robots: 
- NVIDIA GPU-enabled machined that can run Ubuntu 20.04. We have tested on the following laptop models

You would also need the following stereo camera or spinning LiDAR. 
- Stereo camera: FLIR Bumblebee XB3 FireWire
- LiDAR: Waymo Honeycomb, Velogyne Alpha Prime. 

For more information, please refer to the installation guide under hardware requirements. We are actively working towards enabling supports for more sensors. More info on that will be updated on this wiki page. 


# Demonstration for Online VT&R 3
<!-- ====== -->
Please see the following tutorial on how to run online VT&R 3 on Grizzly robot. This tutorial gives basic info on how to use the UI to teach and repeat a path. <iframe width="560" height="315" src="https://www.youtube.com/embed/9dN0wwXDuqo" frameborder="0" allowfullscreen></iframe>


# Installation
<!-- ====== -->
Follow [Installation Guide](https://github.com/utiasASRL/vtr3/blob/main/README.md) to run VT&R 3


# Extension Plan
Below is a list of features that we are currently working in. If you have encountered any other issues while running VT&R 3, feel free to create a new issue on our Github page [add link]. If you have any specific feature request, please directly contact us at vtr3@robotics.utias.utoronto.ca. 

## Pathtracker Overhaul
Add description of this issue.
<!-- > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
> 
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing. -->

## Radar Version of VT&R
We ae working on enabling Radar-based localization in VT&R in the upcoming release. 

## Support for zed stereo camera
We are currently working towards enabling support for ZED stereo camera in our VT&R framework. More detailed instructions on how to set up ZED camera and other sensors will be added to this wiki page. 

# Gallery of Robots that use VT&R
Below are all the robots that use our framework. 

<img width="660" height="515" src="images/collaborators.png">



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

<!-- 
<video autoplay loop muted>
  <source src="VTR3_Argo.mp4" type="video/mp4">
</video> -->

<!-- 1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Fork [this repository](https://github.com/academicpages/academicpages.github.io) by clicking the "fork" button in the top right. 
1. Go to the repository's settings (rightmost item in the tabs that start with "Code", should be below "Unwatch"). Rename the repository "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and create content & metadata (see below -- also see [this set of diffs](http://archive.is/3TPas) showing what files were changed to set up [an example site](https://getorg-testacct.github.io) for a user with the username "getorg-testacct")
1. Upload any files (like PDFs, .zip files, etc.) to the files/ directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
1. Check status by going to the repository settings, in the "GitHub pages" section -->

<!-- Site-wide configuration
------
The main configuration file for the site is in the base directory in [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml), which defines the content in the sidebars and other site-wide features. You will need to replace the default variables with ones about yourself and your site's github repository. The configuration file for the top menu is in [_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml). For example, if you don't have a portfolio or blog posts, you can remove those items from that navigation.yml file to remove them from the header. 

Create content & metadata
------
For site content, there is one markdown file for each type of content, which are stored in directories like _publications, _talks, _posts, _teaching, or _pages. For example, each talk is a markdown file in the [_talks directory](https://github.com/academicpages/academicpages.github.io/tree/master/_talks). At the top of each markdown file is structured data in YAML about the talk, which the theme will parse to do lots of cool stuff. The same structured data about a talk is used to generate the list of talks on the [Talks page](https://academicpages.github.io/talks), each [individual page](https://academicpages.github.io/talks/2012-03-01-talk-1) for specific talks, the talks section for the [CV page](https://academicpages.github.io/cv), and the [map of places you've given a talk](https://academicpages.github.io/talkmap.html) (if you run this [python file](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.py) or [Jupyter notebook](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb), which creates the HTML for the map based on the contents of the _talks directory). -->

<!-- **Markdown generator**

I have also created [a set of Jupyter notebooks](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator
) that converts a CSV containing structured data about talks or presentations into individual markdown files that will be properly formatted for the academicpages template. The sample CSVs in that directory are the ones I used to create my own personal website at stuartgeiger.com. My usual workflow is that I keep a spreadsheet of my publications and talks, then run the code in these notebooks to generate the markdown files, then commit and push them to the GitHub repository.

How to edit your site's GitHub repository
------
Many people use a git client to create files on their local computer and then push them to GitHub's servers. If you are not familiar with git, you can directly edit these configuration and markdown files directly in the github.com interface. Navigate to a file (like [this one](https://github.com/academicpages/academicpages.github.io/blob/master/_talks/2012-03-01-talk-1.md) and click the pencil icon in the top right of the content preview (to the right of the "Raw | Blame | History" buttons). You can delete a file by clicking the trashcan icon to the right of the pencil icon. You can also create new files or upload files by navigating to a directory and clicking the "Create new file" or "Upload files" buttons. 

Example: editing a markdown file for a talk
![Editing a markdown file for a talk](/images/editing-talk.png)

For more info
------
More info about configuring academicpages can be found in [the guide](https://academicpages.github.io/markdown/). The [guides for the Minimal Mistakes theme](https://mmistakes.github.io/minimal-mistakes/docs/configuration/) (which this theme was forked from) might also be helpful. -->
