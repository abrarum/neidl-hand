# Milestone I

## Components used
Things that are required
- Some web camera with at least VGA resolution
- Table
- Linux PC
- Monitor

Things that are optional:
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
    2. Using OpenCV cascades
7. Show output containing recorded image, hand regions, number of hands, number of fingers per hand

## Proposed milestones
1. find suitable light setting
2. develop feature extraction
    - hand separation (2x)
    - hand and finger counting (2x)
3. train the models
4. plug everything together
5. UI
6. Evaluation

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



# Lastenheft

## Initial Situation
The Project is designed to deliver a Product, that helps victims of a stroke to regain more controle of their hand and to rebuild muscles. 
Many people who suffered a stroke loose a lot of control over certain areas of their bodey. Often one half of their hole bodey is partally paralized and usually this involes one hand. 
It is possible to regain controle of the hand with a lot of training and practice. The problem is, that this kind of training needs to be supervised and analyzed. To reduce costs this supervision should be automated so the patient does not need a person to do this all by hand. 

## Goals of the Project
The Product should be able to track multiple hands and the individual fingers live, with a given videostream.
This will be used for analyzation tools that record a patients ability to perform certain training tasks and analyze their progress. 
The reliability of the product will be calculated using the ratio of correctly detected to falsely detected hands, fingers and gestures on different kinds of backgrounds and with different kind of lightings.

## Product usage
The Product should be usable by the patients themselve and should be easy to use, even for people with little understanding of modern technology.
Also the product should work with all skin-colours, with all not-skin-coloured backgrounds, and all lighting levels that are at least dimm rommlighting.

## Functional and non-Funktional requirements

Funktional:
- Detect multiple Hands
- Detect Fingers
- Filter out everything else

Non-Funktional:
- Minimzed setup requirements
- Works on any light lource
- Works on any background
- Provides interface for the analyzing tools
- Works on any skinn colour
- Easy to use
- Works on any System


## Scope of delivery
The project should only produce the Software to detect hands and fingers and give an interface for analysis tools to use that raw data.
This can be accomplished by using the OpenCV and the Tensorflow lybraries and Phython as the coding-language.
This project should not deliver on the hardware like camera. Nether should this project implement any analysis-tool or exercise for actual patients to practice on.

## Milestones
1. Find suitable Setup
2. Develop feature extraction
3. Train the models
4. Combination of the two seperate parts
5. Build a User Interface
6. Evaluation

## Quality requirements
It is required, that the accuracy of the detection hase at least a 90% success rate with different setups from the background, lighting and movement.
