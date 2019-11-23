# Milestone I

## Components used
Things that are required
- Some web camera with at least VGA resolution
- Table
- Linux PC
- Monitor

Things that we are optional:
- Illumination, light bulbs...

## Expected Problems
- shadows might irritate the separation and classification process
  - may be prevented using predefined illumination setups

## Setup
- Camera at a fixed position looking downwards at the table, and the hands
- optional: specify where light bulbs are placed

## Proposed workflow of the system
1. Capture video stream from camera
2. Separate hands from background 
    1. exploiting skin colour and contrasts
        - This provides a binary mask of the hand areas
    2. employing OpenCV cascading
    - We will choose the better option once we get results or run both in parallel  
3. Crop the hand areas
4. Classify hand areas and counting fingers
    1. Feed the cropped images to a neural network
        - NN classifies whether it sees a hand
        - NN counts fingers 
    2. Using OpenCV facades
7. Show output containing recorded image, hand regions, number of hands, number of fingers per hand

## Software and libraries
- Python as a base for input, control, dataflow, glueing all together
- OpenCV for hand separation
    - by skin colour
    - cascading
- For classifying hands and count fingers
    - OpenCV
    - Tensorflow

## Training steps
- OpenCV cascade
    - Finding hand regions
    - count fingers
- Tensorflow
    - classify if hand or not
    - count fingers

