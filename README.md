By using to this link of Roboflow you can find dataset of this experiment .
from roboflow import Roboflow
rf = Roboflow(api_key="I1hO79CqDrKg9qJOiHOd")
project = rf.workspace("cqupt-b8vkv").project("people-count-8vvwf")
version = project.version(1)
dataset = version.download("yolov11")

Step 1: Capture and Annotate Dataset
Video Capture: Record a video to use as a source for creating the dataset.
Convert to Images: Extract individual frames from the video and save them as images.
Annotation: Use the LabelImg tool to annotate the images by drawing bounding boxes around objects of interest.
Step 2: Upload and Prepare Dataset
Upload Dataset: Upload the annotated dataset to the Roboflow platform for preprocessing and version control.
Generate Dataset Link: Obtain the dataset link from Roboflow to integrate it into your YOLOv11 model training pipeline.
Step 3: Train the YOLOv11 Model
Model Training: Use the dataset link to train the YOLOv11 model.
Optimize Accuracy: Tune hyperparameters and monitor training to achieve the best accuracy.
Save Weights: Save the model's best weights for further testing.
Step 4: Test and Evaluate the Model
Unseen Dataset Testing: Evaluate the model's performance on an unseen dataset to verify its accuracy.
Video Inference: Use the trained model for real-time video inference. Automatically detect unique individuals in the video and draw rectangles around them.
Step 5: Deploy with Gradio
Build Web Interface: Use Gradio to create an interactive web interface for the model.
Integration: Include a link to the model for easy access and usability through the web interface
