# Maintnance-of-High-Tension-Towers
Computer Vision | Deep Neural Network | Colab | PyTorch | YOLOv5

![alt text](https://www.tccd.edu/magazine/assets/images/volume-04/issue-01/electric/equipping-header.jpg)

Problem Statement:
Due to the high cost of human-oriented maintenance approach in high tension towers, The Egyptian Ministry of Electricity and Energy requested a prototype for "automated intelligent drones surveillance system" utilizing Deep Neural Network.

Model Archticture:
The arichticture of the system is based upon two networks, one network for detection and localizing of wire braces, another one for identifing and localizng of the condition for each clamp within the brace.

Model Sequence:
1.  Image annotation using Roboflow [Wire Braces] (Object Detection-Bounding Boxes)
2.  The First Network is trained on 5k (512x512 full images).
3.  Saving Network weights to proceed to the next phase.
4.  Image annotation using Roboflow [Each Clamp Condition] (Object Detection-Bounding Boxes)
5.  The Second Network is trained on 5k (608x608 Cropped Detections).
6.  Saving Network weights to proceed to the next phase.
7.  Using Both Networks weights to Localize the Wire Braces in each image, Crop it & resize, to localize and identify the contition of each clamp.
