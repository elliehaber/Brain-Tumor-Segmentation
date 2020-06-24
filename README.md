# Brain-Tumor-Segmentation

The goal of this project is to develop, test, and evaluate a machine learning algorithm that will be able to perform brain tumor diagnosis and segmentation on a test set of MRI images of the brain. 
	It will classify cancerous and non-cancerous brain masses, mainly gliomas, and identify the different regions of the tumor, including: active tumor, edema, and necrosis. The most difficult aspect of tumor segmentation is the large imbalance of tumor labels in the training and test data. This leads to a large number of false-negative results, despite a relatively low percentage compared to the entirety of the data set. 
	We will utilize deep learning and convolutional neural networks to classify the MRI images, as well as a splice-layering technique to create a larger data set. 

Our model architecture is based on the methodology implemented in the following paper: https://arxiv.org/abs/1505.03540<br/>Our code is based on the following repository: https://github.com/jadevaibhav/Brain-Tumor-Segmentation-using-Deep-Neural-networks
