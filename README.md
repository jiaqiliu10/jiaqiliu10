Instructions：
Step1: Run python3 data preparation.py
The purpose of this file is to prepare and split the dataset. The code reads the dataset path from the environment variable ‘DATASET PATH’. If it’s not set, a default path is used. Additionally, the code creates ‘images’ and ‘annotations’ folders under the paths for the training, validation, and test sets.
Step2: Run python3 update annotations.py 
This file is used to update the labels in the annotations to “lego”. The code iterates through all XML annotation files and replaces the labels with “lego”.
Step3: Run python3 train model.py
This file is used for model training, selecting the Mask R-CNN model and loading pre-trained weights (maskr-cnn resnet50 fpn)
Step4: Run python3 test model.py
This file is used for testing a single image. It loads the MaskR-CNN model, successfully draws the prediction boxes, and sets the score threshold to 0.5.
Step5: Run python3 evaluate model.py
For model performance evaluation, outputs the mAP scores at different IoU thresholds and draws detection bounding boxes.
