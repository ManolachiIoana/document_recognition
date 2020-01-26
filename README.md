Train on the RVL-CDIP dataset using Convolutional Neural Network to classify document images into 16 categories.
Test and train datasets can be found here: https://www.cs.cmu.edu/~aharley/rvl-cdip/ (too large to be included in the project)
The data consists in 400 000 images splitted into training, testing and validation datasets, with each image located in its own folder within a deep hierarchy of folders without any particular order. 
	
##  Notebooks

 1.1 Extract and sort.ipynb 
- I decided to subset the data to 3200 images per training class and 1600 images per test/validation classes (100 images from each of the 16 cathegories). The 'data' directory will contain training, testing and validation folders with individual class folders within each of those, each named with the document type.

2.1 Explore Data.ipynb 
- I explored the data in order to have a better view on the distributon of black and white pixels and draw some conclusions

3.1 Process Data - CNN model.ipynb 
- basic CNN model with 5 convolutional layers, 4 max pooling layers, one flatten layer and one prediction layer (softmax)
- test accuracy (after 10 epochs): 46.25%
- confusion matrix conclusions: the model achieved better accuracy for some classes (more than 75% for email, handwritten, questionaire) and low accuracy for others (less than 20% for advertisment, resume)
    
3.2 Process Data - VGG16 transfer learning.ipynb
- implement transfer learning of VGG16 from scratch in Keras. 
- import VGG16 from keras with pre-trained weights which was trained on imagenet.
- I will not be training the weights of the first 19 layers
- test accuracy (after 10 epochs): 68.75%

 ## csv_files
    - contains train, test and validation csv with random chosen image paths (3200 images per training class and 1600 images per test/validation classes)


 ## Project dependencies:
- python 3
- jupyter notebook 6
- other dependencies are in requirements.txt