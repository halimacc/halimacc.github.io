title: Kinect2 and Projector Calibration with Enhancement
date: 2016-09-29 22:57:56
categories:
	Calibration
---
![AR](http://7xqh47.com1.z0.glb.clouddn.com/kinect2-project-calib/ar.png)

With a Kinect and a projector, it's easy for one to build a simple SAR(Space Argumented Reality) program like [above](https://www.youtube.com/watch?v=FnulH8TrZVo). To get start, an essential step is to calibrate the Kinect and projector. 


Kinect2 Projector Calication Tool
---------------------------------
[KinectProjectorToolkit](http://www.genekogan.com/works/kinect-projector-toolkit.html) is a Processing project that could calibrate a projector to a Kinect depth camera, I've migrated it to Kinect2 and you can visit [**Kinect2ProjectorCalibration**](https://github.com/halimacc/Kinect2ProjectorCalibration) and use it to calibrate your Kinect2 depth camera and projector.

To give myself some credit, I have to say it's not easy to find such a project and migrate to Kinect2 among many Kinect/camera projector calibration projects due to

- **Interactivity**: the size of Kinect2's color stream has increased to 1920x1080, this rules out many projects that need finding chessboard in realtime video stream.

and

- **Compatibiliy**: most of calibration projects are `openframeworks` project, while there's no Kinect2 library that satisfies the interface as Kinect libraries provide in these projects.


Accuracy Improvement
--------------------
Useful and convenient the project is, however, the calibration result can sometimes be very inaccurate, a main cause is the **pixel flicker** comes from hardware error. To address this problem, two methods have been taken to improve the stability of image.

#### Averaged Image Frame

Leveraging the fact that 1) the scene in a calibration is completely static, and 2) the pixel flicker is random, we can assume that the average image of sufficient number of frames is very close to the groundtruth image. So I used an averaged image of many sequentials frame as the final image used to calibration in the project.


#### Bilinear interpolation on registered image

The Kinect2ProjectorCalibration project detect chessborad pattern in a **registered** image (which is a depth image with color pixel mapped on it), 



Reference
---------
[矫正kinect深度相机与其它图像摄像机以及投影机的空间关系](https://github.com/yty/yty.github.io/issues/4)





