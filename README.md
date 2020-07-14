# Brain_Tumor_Detection_Project

<p>This Project uses transfer learning to build a CNN model to classify whether a patient have brain tumor or not based on MRI scan.</P>

**About the Data**
<p>The dataset is in Brain_tumor dataset folder. This folder have 2 subfolder yes and no containing 253 MRI scan images. Folder yes have 155 tumrous MRI scaned images and folder no have 98 non-tumorous MRI scanned images.</p>
Link to Dataset: https://www.kaggle.com/navoneel/brain-mri-images-for-brain-tumor-detection


## Data Augmentation

<p>As the dataset size was small ,data augmentation was done to increase the size of data and also to decrease skewness of data.<br>
  
**Before augmentation:**<br>

 155 positive examples and 98 negative examples.<br>
 From data augmentation 1 positive example is converted into 7 and 1 positive example ois converted into 10 so <br>
 
  **After augmentation:**<br>
  
  1085 positive and 980 negative exapmples.<br>
  Augmented data is saved in folder augmented_data.
  
  ## Data Preprocessing
  
  For every image following process is applied.
  1. Crop the brain through opencv(finding contours).
  2. Resizing all images into a common size to fir to neural network.
  3. Applying normalization.
  4. Appending images pixels to X(feauture vector) and giving them labels(y).
  5. Shuffling X and Y.
  
  ## Transfer Learning
  
  1. **VGG16**<br>
     This model was applied with same wieghts as learned from imagenet dataset. Last 3 layers of VGG16 were removed and trainable  layers were inserted.
     ![alt text](https://github.com/dhruvgrover1251/Brain_Tumor_Detection_Project/blob/master/VGG16withtoplayers.png)<br>
     
     **Training of model** <br>
     
     ![alt text](https://github.com/dhruvgrover1251/Brain_Tumor_Detection_Project/blob/master/VGG16training.PNG)
     Test Accuracy = 0.9935483932495117<br>
     F1 score: 0.9467084639498432<br>

  2. **InceptionV3**<br>
     This model was applied with same wieghts as learned from imagenet dataset. Last 3 layers of inceptionV3 were removed and trainable  layers were inserted.
  3. **Resnet50**
     This model was applied with same wieghts as learned from imagenet dataset. Last 3 layers of resnet50  were removed and trainable  layers were inserted.
     
 ## Trying own model 
 This model was tried in expectation that less number of parameters may have greater accuracy but did not perform as good as above models.
 



