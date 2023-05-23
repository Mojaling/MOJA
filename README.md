ImageAI

ImageAI is a Python library that provides easy-to-use methods and functions for working with artificial intelligence and computer vision in images and videos. It simplifies the process of implementing image and video recognition, object detection, and other related tasks.

Key Features

Object Detection: ImageAI supports various object detection models, including RetinaNet, YOLOv3, and TinyYOLOv3. You can use pre-trained models or train your own custom models for object detection tasks.

Video Object Detection: ImageAI allows you to perform object detection in videos by processing each frame. This feature is available for both pre-trained models and custom models.

Image Classification: ImageAI provides pre-trained models for image classification tasks, including SqueezeNet, ResNet, and InceptionV3. You can also train your own custom models for classification.

Custom Model Training: You can train your own custom models for object detection and image classification using ImageAI. It supports transfer learning, enabling you to leverage pre-trained models and fine-tune them for your specific tasks.

Prediction and Analysis: ImageAI makes it easy to make predictions on images and videos using pre-trained models or custom models. It also provides functions for analyzing the results, such as extracting object boundaries and obtaining the percentage of object area within images.

Installation

To install ImageAI, you can use pip, the Python package installer:

bash

pip install imageai --upgrade


Please note that ImageAI requires Python 3.7 or later.

Usage

Here is a basic example of how to perform object detection using ImageAI:

python
Copy code
from imageai.Detection import ObjectDetection
import os

# Create an instance of the ObjectDetection class
detector = ObjectDetection()

# Set the path to the pre-trained model file
model_path = os.path.join(
    os.getcwd(), "models", "resnet50_coco_best_v2.1.0.h5")
detector.setModelTypeAsRetinaNet()

# Load the model weights
detector.setModelPath(model_path)
detector.loadModel()

# Set the path to the input image
input_path = os.path.join(os.getcwd(), "input", "image.jpg")

# Perform object detection on the input image
detections = detector.detectObjectsFromImage(
    input_image=input_path, output_image_path=os.path.join(
        os.getcwd(), "output", "image_detected.jpg"))

# Print the detected objects and their probabilities
for detection in detections:
    print(detection["name"], " : ", detection["percentage_probability"])


For more detailed examples and usage instructions, refer to the official documentation.

Contributions

Contributions to ImageAI are welcome! If you encounter any issues, have suggestions for improvements, or would like to add new features, feel free to open an issue or submit a pull request on the GitHub repository.

Before making a contribution, please read the contribution guidelines.

License

ImageAI is released under the MIT License. Please refer to the license file for more details.

Acknowledgements

ImageAI is developed and maintained by OlafenwaMoses. The library is built on top of various open-source frameworks and libraries, including TensorFlow, Keras, OpenCV, and NumPy.

Support

If you need
