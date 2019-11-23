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
  - may be prevented using certain illumination setups

## Setup
- Camera at a fixed position looking downwards at the table and the hands
- optional: specify where light bulbs are placed

## Proposed workflow of the system
1. Capture video stream from camera
2. Separate hands from background expoilting skin colour and contrasts
  - This provides a binary mask of the hand areas
3. Crop the hand areas
4. Feed the cropped images to a neural network
5. NN classifies whether it sees a hand
6. NN counts fingers 
