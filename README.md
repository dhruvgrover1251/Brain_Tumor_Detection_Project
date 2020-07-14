# Brain_Tumor_Detection_Project
<p>This Project uses transfer learning to build a CNN model to classify whether a patient have brain tumor or not based on MRI scan using tensorflows.</p>

**About the Data**
<p>The dataset is in Brain_tumor dataset folder. This folder have 2 subfolder yes and no containing 253 MRI scan images. Folder yes have 155 tumrous MRI scaned images and folder no have 98 non-tumorous MRI scanned images.</p>
Link to Dataset: https://www.kaggle.com/navoneel/brain-mri-images-for-brain-tumor-detection

##Data Augmentation
<p>As the dataset size was small ,data augmentation was done to increase the size of data and also to decrease skewness of data.<br>
 Before augmentation:<br>
  155 positive examples and 98 negative examples.<br>
 From data augmentation 1 positive example is converted into 7 and 1 positive example ois converted into 10 so <br>
  After augmentation:
  1085 positive and 980 negative exapmples.<br>
  Augmented data is saved in folder augmented_data.


