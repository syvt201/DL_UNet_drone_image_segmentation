# Deep Learning-Based Image Segmentation for Drone-Captured Images
This project focuses on segmenting two types of objects—trees and grass—using a deep learning model. Since trees and grass share similar colors, accurately distinguishing between them presents a challenge. To address this, I employed the UNet model, a widely recognized deep learning architecture for segmentation tasks. The model was trained on a dataset of drone-captured images. I labeled the tree and grass classes using the AnyLabeling tool, drawing bounding boxes around the objects and generating grayscale mask images for the segmentation process.

Draw bouding-boxes around the objects in AnyLabeling
![](AnyLabeling_labeling.png)

# Dataset
The dataset consists of drone-captured images from various regions in Vietnam. Since the images vary in size and the model requires uniform input dimensions, I cropped each image and its corresponding mask into smaller patches of 256x256 pixels. The dataset was then split into training and testing sets, with the training set containing 4,044 patches and the testing set containing 1,737 patches

Original image and its mask.
![](org_image_and_mask.jpg)

# Training
The UNet model was trained on Google Colab. Due to the large size of the dataset, I limited the training to 25 epochs.

Training accuracy and loss of UNet model
![](accuracy_loss.jpg)

# Result
After training and evaluating the model's performance using the testing set, the UNet achieved an accuracy of 89.47% and a loss of 0.63. Additionally, I computed the IOU index, which demonstrated a high IOU value for the testing images.

One testing image recorded a particularly high IOU index of 88.43%.
![](infer_image.jpg)

For more detailed information about this project, please refer to the [project-report](project_report.pdf) file.