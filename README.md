Dataset Description

The Pothole Detection Dataset is an open-source dataset published by the Intel Unnati Training Program on Roboflow Universe. It is designed for training computer vision models to detect potholes and road anomalies. The dataset consists of labeled images in YOLO format, making it suitable for object detection tasks using models like YOLOv8. This dataset is widely used for autonomous vehicle safety, smart city infrastructure, and deep learning research in road maintenance automation.

Dataset Composition

The dataset initially contained a total of 2,475 images, labeled into eight classes:

Drain Hole

Circle Drain Clean

Drain Clean

Drain Not Clean

Hole

Manhole

Pothole

Sewer Cover

Since this project focuses solely on pothole detection, the other seven classes (Drain Hole, Circle Drain Clean, Drain Clean, Drain Not Clean, Hole, Manhole, and Sewer Cover) were removed. This resulted in a refined dataset of 2,218 images, where all annotations are exclusively labeled as "pothole."

Preprocessing Techniques
To enhance the model's robustness and improve detection accuracy, several preprocessing techniques were applied to the dataset:

Auto-Orient: Corrected image orientations to ensure uniform alignment.

Stretch Resize: Resized all images to 640×640 pixels for consistency.

Data Augmentation
To increase dataset diversity and improve model generalization, various data augmentation techniques were implemented:

Flip: Horizontal flipping to introduce variations in perspective.

Crop: Minimum zoom of 0% and maximum zoom of 15% to simulate different camera distances.

Rotation: Random rotation within a range of -15° to +15° to account for different camera angles.

Saturation Adjustment: Random variation between -30% to +30% to adapt to different lighting conditions.

Brightness Adjustment: Random variation between 0% to +15% to enhance adaptability to different exposure levels.

Noise Addition: Up to 0.1% of pixels modified to simulate real-world distortions.

After applying these augmentations, the final dataset expanded to 3,770 images, ensuring better model performance by exposing it to varied road conditions.

Dataset Splitting
For training purposes, the dataset was divided into three subsets:

Training Set (82%) – 3,104 images used for model learning.

Validation Set (12%) – 444 images used for hyperparameter tuning.

Test Set (6%) – 222 images used to evaluate model performance.

This dataset forms the backbone of the pothole detection system, enabling the deep learning model to accurately identify and classify potholes in real-time. The curated dataset, combined with preprocessing and augmentation techniques, ensures that the model is trained on diverse and realistic road conditions, ultimately leading to improved pothole detection efficiency and reliability.

