---
layout: project
title: SideWalk Detector
date: February 13, 2016
image: https://cloud.githubusercontent.com/assets/4311090/13205691/5a81a83a-d8b3-11e5-87a2-6a8b6e73b525.png
---

##The Background:
We’ve recorded a rosbag of an Intel RealSense (R200) camera via their official ros node (dig in to see a description of its topics). Both the depth and color camera are being sent at 30fps. It should be roughly 20 seconds worth of footage of the camera “walking” down the sidewalk outside our office. Also, note that the camera was approximately 21” off the ground during the rosbag recording. 

##The Project:
Build a ROS node called “sidewalk_detector” that consumes the replayed data of this rosbag and outputs the following topics:

1. /sidewalk_detector/color/image_raw
2. /sidewalk_detector/depth/points_in
3. /sidewalk_detector/depth/points_out

###Definitions: 
where 1. outputs the images from the topic "/camera/color/image_raw” with a visible highlight (e.g. a red mask) mapped over the set of pixels that are considered to be INSIDE the sidewalk

where 2. outputs a point cloud which contains the subset of points from the point cloud output by the topic "/camera/depth/points” that are considered to be INSIDE the sidewalk

where 3. outputs a point cloud which contains the subset of points from the point cloud output by the topic "/camera/depth/points” that are considered to be OUTSIDE the sidewalk

By “inside” we mean any point or pixel that maps to a piece of sidewalk, whether or not we could navigate there. So, if we were doing it by hand, we’d open an image editor and fill in all the pixels that we perceive as being the sidewalk. 

[Click Here for the Code](https://github.com/ChuChuIgbokwe/sidewalk_detector)
