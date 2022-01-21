# Multiperson_Pose_Detection
![image](https://user-images.githubusercontent.com/98158660/150531398-de4574d6-8b06-42eb-ac81-daea5817764a.png)

Application of Movenet model to detect multiple objects in a frame
Refer the link- https://tfhub.dev/google/movenet/multipose
tutorials posted by Nicholas- https://www.youtube.com/watch?v=KC7nJtBHBqg&list=PLXxGuqpiGy3DYadMxf1cwACoDzP0-ajcx&index=6


Information on the output
#output_0 represents one set of detections, is a dictionary with shape=(1,6,56)
- 6 set of arrays wrapped inside 1 array, 
- 6 here means 6 people max which the model can detect.
- 56 here is keypoints or values= these represent y,x,score coordinates
- score (detection confidence) 
(This is 3*17 coordinates=51+5 key points for bouding box)
- We need to grab 51 coordinates (for 17 keypoints) to make joint detections
- Order of 17 keypoints joints is:
[nose, left eye, right eye, left ear, right ear, left shoulder, 
right shoulder, left elbow, right elbow, left wrist, right wrist,
left hip, right hip, left knee, right knee, left ankle, right ankle]
