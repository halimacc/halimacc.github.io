title: Calibrate Kinect2 and Projector
date: 2016-09-29 22:57:56
categories:
	Calibration
---
With a Kinect and a projector, it's easy for one to build a simple SAR(Space Argumented Reality) program like [this video](https://www.youtube.com/watch?v=FnulH8TrZVo). To get start, an essential step is to calibrate the Kinect and projector. You can find plenty of projects that calibrate Kinect/camera and projector, however, bare of them can be easily transplanted to Kinect2 due to

- **Interactivity**: the size of Kinect2's color stream has increased to 1920x1080, this breaks many projects that needs to finding chessboard in realtime video stream.

and

- **Compatibiliy**: most of calibration projects are `openframeworks` project, while there's no Kinect2 library that has satisfied the interface provides Kinect libraries used in these projects.

Fortunately, I found a Processing project [KinectProjectorToolkit](http://www.genekogan.com/works/kinect-projector-toolkit.html) that meets the requirement and transplanted it to Kinect2. You can visit it at [Github](https://github.com/halimacc/Kinect2ProjectorCalibration) now.

// to be continue with flicker problem

