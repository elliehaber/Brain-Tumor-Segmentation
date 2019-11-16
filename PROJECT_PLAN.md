
# Brain Segmentation for Tumor Diagnosis Project Plan
### Team Members: Ellie Haber, Denys Fenchenko, Erin Crowe

## Project Title: Brain Tumor Diagnosis and Segmentation 

### Project Abstract: 

The goal of this project is to develop a machine learning model with brain tumor segmentation capabilities,
as a means of accurately segmenting gliomas from the healthy tissue of the brain. A brain tumor is a cancerous 
or non-cancerous growth of abnormal cells in the brain, which can be classified as benign or malignant. The benign
tumor has uniformity in structure and does not contain active or in other words cancer cells, whereas malignant brain
tumors have non-uniform structures and contain active cells. For our purposes, we will be classifying gliomas, a 
type of brain tumor that is most often rapidly growing and malignant. Gliomas are categorized into low and high grades, 
the higher grades are more quickly spreading and require more intensive treatments than low-grade. Brain tumor
segmentation consists of separating different tumor tissues, such as active tumor, edema and necrosis from normal
brain tissues: GM, WM, and CSF. 


To create and train our model, we will be using the BraTS 2013 data set. This set is used for the MICCAI annual 
Challenge on Multimodal Brain Tumor Image Segmentation (BRATS 2013). It is a medical image repository composed of 
anonymized MRI images. The dataset has three sub-datasets: the training set, the testing set, and the leaderboard
set. The training data is comprised of 30 patient MRI images with an accurate ground truth, with twenty high grade 
tumors and ten low grade tumors. The testing dataset has ten low grade tumors, and the leaderboard set has 25 subjects,
with 21 high grade and four low grade tumors. 

One of the biggest difficulties in the area of brain tumor segmentation is the large imbalance of tumor labels in
training and testing data sets for MRI scans of the brain. Since it is more likely for a person to have a healthy 
brain as opposed to a brain with a tumor, a machine learning model can maintain high accuracy even if it incorrectly 
classifies an image as a false-negative. Moreover, in a brain MRI scan, healthy voxels make up 98% of the image’s
total voxels, which causes models to be overwhelmed by healthy tissue even when a brain tumor is present.
Segmentation traditionally requires identifying the entire tumor region, then the tumor core, and then the active tumor. 
Full segmentation is completed when all three regions have been identified. 

Some of the most common methods to achieve multimodal brain tumor segmentation are using a convolutional neural 
  network (CNN), and deep learning. As an aside, you can analyze the symmetry of a particular MRI by identifying if 
  there is a tumor present in the left or right side of the brain. It is important to know then that if there is a 
  tumor present in the left side, there is a small likelihood that there will be one in the right side of the brain, 
  and vice-versa,  so the image will be asymmetric. In particular, we will use a cascading architecture with two 
  separate convolutional neural networks (CNN), which will allow the output of the first CNN to act as the input
  of the second. Convolutional neural networks are some of the best methods of classifying images, compared to 
  speech or other classifiable media. This is done by utilizing a convolutional layer. Several of these layers can be 
  stacked to organize the features into a hierarchy, and outputs planes called feature maps. 

Evaluation of the convolutional neural networks will be split into two separate training phases. In the first phase,
  our dataset will be constructed so the probability of any label being produced is equiprobable, even though as mentioned 
  prior, it is more likely for a voxel to be classified as healthy given that any given brain has more healthy voxels than 
  unhealthy ones, even in the presence of a tumor. During our second phase of training, we account for the unbalanced nature 
  of our data and will re-train our output layer with a better representation of the labels we can produce. This approach is 
  based upon the research paper Brain Tumor Segmentation with Deep Neural Networks, co-authored by Aaron Courville and Yoshua 
  Bengio.  We will use categorical cross-entropy as our loss function for all the pixels in a given slice of the MRI we are
  trying to classify. Additionally, we will use batch-normalization in order to get the most accurate labels from the data 
  in our model. 




### Milestones (these are rough dates): 

#### Basic Research : Be ready to perform initial processing by Saturday, November 16

At this stage of a project we will primarily focus on acquiring medical background in the area of brain tumor segmentation, understanding how convolutional neural networks are implemented, and what architecture we are going to need in order to build (CNN) for brain tumor segmentation. 
Project Plan (Due November 12) ✅


#### Access dataset, perform regularization/create models: November 16-21

#### Neural Network Training: November 21-November 25
Allow at least 4 days** Could use mini batching to train the network faster
 (may not need all the time for step 2, could start the training earlier if necessary)

#### Evaluate the performance of our algorithm: November 25-November 29

** If Necessary ** make edits if algorithm doesn’t perform as we wanted
Must be completed by December 1 to allow time to write the final Project Report with full data and algorithm performance analyzed 

#### Project Report, Due December 3, 2019

#### Project Presentation Video, Due December 10, 2019


