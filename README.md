# FINE TUNED YOLO_NAS-S JAR LID DEFECT INSPECTION

Defect inspection is an indispensable process across industries like manufacturing, automotive, electronics, and pharmaceuticals, ensuring that products meet the desired quality standards and customer expectations. Its primary purpose is to identify and remove faulty or defective items prior to their release into the market. In this project, we will leverage computer vision for jar lid defect inspection.

# Dependencies
 - Super-Gradients
 - Glob
 - PIL
 - Pandas
 - Numpy
 - Json
 - OS
 - Shutil
 - Imagesize
 - Time
 - Matplotlib
 - Sys
 - Seaborn
 - Ptitprince
 - re

# Dataset
This dataset obtained from kaggle has been collected by RUTHGER RIGHART. It contains 168 images with composed of 1859 jar lids. Each image has an average of 11 jar lids. The dataset has two labels: damaged lids 897 images and intact, 962 images. Damaged lids can be categorized as deformations, holes and scratches. A annotated csv file with bounding boxes is provided with the images. The csv file will be later used to create the YOLO annotation training labels format.
Seeing the small size of the dataset, image augmentation is used to increase the dataset size.
 - Training size : 134 images
 - validation size : 17 images
 - Testing size : 17 images

# Model
For training the model, we used a model from state-of-the art one-stage detector family. The model is based on a fine tunined YOLO-NAS small.
YOLO-NAS is the most recent object detector model released. It performs better compare to previous models and the super-gradients package makes the training friendlier.

# Training Parameters
Below parameters can be adjusted according your needs. The model is trained on Google Colab with GPU for 50 epochs.
![training_parameters](https://github.com/WENDGOUNDI/yolonas_jar_lid_defect_inspection/assets/48753146/05ad415d-7060-4ba6-aa5a-b1f39c298d93)

# Performance
The model has been trained for 50 epochs
### last epochs : training results
![training_result](https://github.com/WENDGOUNDI/yolonas_jar_lid_defect_inspection/assets/48753146/fd798799-b44f-436b-ac0b-145a32c5d3a1)

### last epochs : validation results
![validation_result](https://github.com/WENDGOUNDI/yolonas_jar_lid_defect_inspection/assets/48753146/0e283744-a9a7-41ff-a04d-4266abc52ee0)

# Inference
![test_inference](https://github.com/WENDGOUNDI/yolonas_jar_lid_defect_inspection/assets/48753146/ac03911d-877d-4c09-afb2-637e7f1d0954)


# FUTURE DIRECTIONS
 - Try YOLO-NAS medium and large.
 - Generate synthetic data for training.

# References:
 - dataset link : https://www.kaggle.com/datasets/rrighart/jarlids
