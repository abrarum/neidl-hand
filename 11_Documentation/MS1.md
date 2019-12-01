# Questions to be answered
## Which components are involved

The project involves 3 main components i.e Video camera, image processor code, and an output display software.

## How do they interact

The general flow of the project starts from the video camera which captures each frame and the image processor code involves multiple functions to process those frames to detect/track hands and segment fingers. After processing, code then displays the output of the video, frame by frame indicating the of the no. of hands/fingers and bounded box over hand(s) in real-time.

## Specification of functions

Processor code has various stages to process and create an output for each frame. Each stage make use of multiple libraries and function. Some of the main functions involved in the processor code includes:

1. Video capture:

This stage/function involves capturing videos frame by frame. Opencv is responsible to process the input and output of the video streams.

2. Hand detection:

This function is responsible to detect the hands in the frame. There are tens of strategies to do this. Some of them are:

  > Hand segmentation:
  
    1. Background subtration: As the name suggests, it involves removing the bg from the image.
    2. HSV segmentation: Involves finding the color of the skin and and use it as a threshold to binarize the image.
    
  > HAAR Cascade:
    
    An object detection algorithm that creates a detailed map of features of the hands. These detailed pre-trained features help in detecting the hand landmarks in each frame.
    
  > Neural Network:
   
    Strategy that involves training on thousands of images and creates a model that can predict hands/fingers from unknown frames. This strategy is computational heavy since the video camera has to detect each frame from scratch.
        

After testing and observations, we've decided to implement the hand segmentation technique for hand detection phase.


3. Finger detection:

This function involves the detections of fingers seperated from hands and creating a combination of gestures to count the fingers.

  > Manual convexity defect detection:
    
    After getting the mask of hands, fingers can be deteced by detecting the largest contour in the frame which is presumably the fingers, then creating a convex of the hands and detecing the convexity defect by detecting the buldge of the fingers. Each convexity defect indicates 2 fingers raised since there is 1 convexity defect in 2 fingers.
    
   > CNN (Convolutional neural network)
   
    A relatively easier option but computational intensive and needs a good amount of data to process on. This strategy involves training hundreds and thousands of images with combinaton of finger gestures with labels and are then trained to create models which are then can be used to predict the finger gesture in the video frames.
    
    
Manual convexity detection is something we thought would be a liable option since it involves less computation and faster for real-time detection.
 

## Detailed milestones for the project

1. Project prototype with hand detection only -- 23rd December 2019
2. Finished project with hand and finger detection -- 13th January 2019
3. Presentation of the final project -- 20th January 2019
4. Documentation review and submission -- 27th January 2019
