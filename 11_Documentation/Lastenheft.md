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
- Works on Linux systems with Python3


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
