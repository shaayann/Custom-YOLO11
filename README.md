# YOLOv11 Fine-Tuning

Summary
This project demonstrates the fine-tuning of a YOLOv5 model for object detection using a custom dataset. The process begins with preparing a labeled dataset in the YOLO format, which is then split into training and validation sets. A pre-trained YOLO model is used as the base for fine-tuning on the custom dataset. The model is trained for 50 epochs, with the training and validation data configured through a YAML file. After training, the model is saved for future use and deployed to make predictions on new images.

Dataset
The dataset consists of images labeled with objects to be detected. The dataset was split into training (90%) and validation (10%) sets. A total of 85 images were used, with 76 allocated for training and 9 for validation. The dataset also includes a class file that defines the categories of objects present in the images.

Model Training
The fine-tuning process involved the following:

Pre-trained Model: The YOLOv5 model (yolo11n.pt) was used as the base model for training.
Epochs: The model was trained for 50 epochs with a batch size of 16 and an image size of 640 pixels.
Configuration: A custom data.yaml file was created, specifying the dataset paths, number of classes, and class names.
Results
After training, the model was tested on new images. The inference results included:

Object Detection: The model successfully detected objects in test images with bounding boxes.
Confidence Scores: The model provided confidence scores for each detected object, indicating the reliability of the predictions.
Class Labels: Each detected object was assigned a class label based on the trained model.
The model's performance demonstrated the ability to accurately predict object locations and class categories on new data, confirming that the fine-tuning process was successful.

Conclusion
The fine-tuned YOLOv5 model is now capable of performing object detection on images containing objects from the specified classes. The results indicate that the model is effective for detecting and classifying objects based on the custom dataset. Future work may involve further refinement of the model or testing on additional datasets to improve accuracy.
