## An Android version of ORB-SLAM2

# Introduction

This has some updates to the original slamit app. Some build issues replated to C++ modules were fixed.                                                  
The main slam UI has been reorganized. Background color for the point cloud mapping has been changed to black instead of white. Mapping points are blue and red instead of black and red.

# Notes on running

1. You will have to create a folder named SLAM on the internal storage (eg., /storage/emulated/0/SLAM)
2. ORBvoc.txt file needs to be copied to this folder (refer ORB_SLAM2 and get the zip file and unzip it and put it). Without this the app will crash.
3. Calibrate your camera using OpenCV or some calibration tool. Use the TUM1.yaml file in ORB_SLAM2 C++ application under examples and sync your calibrated data for fx, fy, cx, cy, k1, k2, p1, p2, and p3.
4. Put the calibrated file into the SLAM folder. By default slamit uses the file named List3.yaml as the calibration file if its not slected during the run of the application
5. Once the calibration file is selected and ORBvoc.txt is in your SLAM folder. The applicastion should start initialize SLAM and after a few seconds, show the tracker on your right in a black screen. A preview of the video fed will be shown on the left side.
6. Once the tracking starts which will happens after a few seconds after SLAM initialization, the point cloud should start showing up on the right side in blue and red.
7. As you move around, it should continue tracking and plotting the point cloud with the camera preview moving for each tracked frame as appropriate.

# Credits
The capstone design project for UM-SJTU Joint Institute in Shanghai Jiao Tong Univeristy sponsored by Huawei Technologies

Thanks to the teamwork of Luwei Yu, Xiaobai Ma, Zhenkai Wang, Zhi Zhang and myself, we made an Android App named *slamit*, which could achieve realtime Simutaneous Localization and Mappint (SLAM) using the ORB-SLAM2 algorithm. It worked successfully on Huawei P9.
