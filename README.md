# Overlapping-Object-Cropping-Tool
How This Works:
Model Loading: Uses TensorFlow.js with the COCO-SSD model (pre-trained object detection model) to detect objects in images.

Object Detection:

Detects common objects like faces, people, hands, etc.
Can handle overlapping objects by analyzing their bounding boxes
Primary Object Selection:

Filters detected objects by the selected type (face, person, or hand)
Selects the largest object (by area) as the primary object
Falls back to similar objects if the exact type isn't found
Cropping:

Extracts the primary object from the original image
Scales it appropriately to fit the output canvas
Centers the cropped object in the result view
User Interface:

Drag-and-drop or file selection for image upload
Progress indicators during processing
Side-by-side comparison of original and cropped results
Supported Object Types:
Faces (primary focus)
People (full body)
Hands (when selected as primary object)
The code handles cases where objects overlap by using the object detection model to identify all objects and then selecting the most prominent one based on size and position.
