# yolov3_butterfly

I have attempted to perform object tracking of butterfly on a video 
Lots of Butterfly Flying in Flowers Garden | How Butterflies Pollinate Flowers. - YouTube
(https://www.youtube.com/watch?v=6hyLdfYIcxI) 

Aim
- The number (count) of butterflies on screen at any given time
- An obvious indication of when a butterfly flies in or out of frame

Dataset:
Open Images DatasetV7 

Classes:
Butterfly

No of photo used:
400

![image](https://user-images.githubusercontent.com/33034362/226266416-1a2b375d-736e-49bf-a315-e817460e81d1.png)


Package and modules used
YOLOv3
Darknet(https://github.com/AlexeyAB/darknet)
Deep SORT(https://github.com/theAIGuysCode/yolov3_deepsort) 
Tensorflow

Running environment
1. Google Colab


Steps 1:
1. Train a existing real-time object detection algorithm(YOLOv3) using custom dataset
After labeling and the custom train data 
The traing loss as shown below:

![image](https://user-images.githubusercontent.com/33034362/226270792-3609a560-9feb-4a03-b925-c76e113f2f73.png)


And the prediction sample as show below:

![prediction_test_1](https://user-images.githubusercontent.com/33034362/226271331-537b266a-46e9-4c65-bdde-39cddb910ff7.png)






Result:
1. Successfully object detection on the video to detect the butterfly show in result.avi in this repository

Code for generate result video

!./darknet detector demo data/obj.data cfg/yolov3-custom.cfg /mydrive/yolov3/backup/yolov3-custom_last.weights /mydrive/yolov3/video_1.mp4 -out_filename /mydrive/yolov3/results.avi -thresh 0.7


Still to improve:
sometime can only identify one butterfly in a goup of butterflies

possible reason:  
not enough training data (only 400 training data was used)

Step 2. Track and count real-time 
1. Train and transform the darknet weights into tensorflow tf file
2. Tracking with Deep SORT and Tensorflow can run but not able to generate result video. 

Running environment

Local computer

possible reason:
1. hardware issue without required plugin for media












