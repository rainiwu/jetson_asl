# Obtaining the dataset
Due to its large size, the dataset is not included here. To obtain the dataset, follow this link: [https://www.kaggle.com/grassknoted/asl-alphabet](https://www.kaggle.com/grassknoted/asl-alphabet). Note that a Kaggle account is required to download this dataset. This directory is included to provide a default location for the dataset to reside.

Once the dataset is downloaded, ensure that the training data is present in this directory as './asl_alphabet_train/asl_alphabet_train/'. 
This structure is slightly different from the default of the downloaded dataset. If you would like to use an alternative dataset location, be sure to modify the appropriate strings in the ../sign_language.ipynb notebook.

The training data is 29 folders named 'A' to 'Z', plus 'del', 'nothing', and 'space'. Each folder should contain 3000 200x200 color images. If your dataset is different from this structure, ensure that you have obtained the correct dataset. 
