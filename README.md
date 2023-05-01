# SkinCancerDetection
Skin Cancer Detection System which has an accuracy of 97.96

 



Abstract


The most common type of cancer in the country is skin cancer.
In the United States, more than 4 million cases of skin cancer are found each
year. In order to reduce effort, time, and human life, an accurate automated
system for skin lesion recognition is absolutely necessary for early detection.
The goal of this project is to develop a machine learning model that can
classify skin lesions at an early stage in order to accurately diagnose the
illness and aid in clinical decision-making, increasing the likelihood that the
condition can be treated before it spreads.




Introduction


Skin cancer is one of the most frequent cancers not only in
the United States, but also worldwide, with about 10,000 people diagnosed with
it in the United States every day. Despite the fact that the number of Melanoma
deaths is expected to rise by 22% in the coming year, early identification of
the disease can lead to a 99% survival rate. Early detection of skin cancer is
critical and can prevent further spread in some cases, such as melanoma and
focal cell carcinoma. In any case, there are several factors that have a
negative impact on detection accuracy. In recent years, the use of image
processing and computer vision in healthcare and medical applications has
increased significantly.


In this study, we use various machine learning models to
detect and categorize cancer based on dermatoscopic images of pigmented
lesions.



 



Description of Dataset



The Harvard database released accessible the HAM10000
("Human Against Machine with 10000 training images") dataset, which
contains 10,015 dermatoscopic images, in June 2018. A metadata file including
demographic information for each lesion is also provided. More than 50% of
lesions are confirmed by histopathology (histo); the balance of the cases are
confirmed by follow-up examination (follow up), expert consensus (consensus),
or in-vivo confocal microscopy (confocal).



The HAM10000 dataset includes a file (HAM10000 metadata.csv)
that contains additional dataset information, the most essential of which is
the type of skin lesion displayed in each image. It is critical to comprehend
the information contained in the metadata to determine which sections of the
metadata may be used as a feature in our learning process. Here, we visualize
the dataset's metadata, specifically the features age, gender, body
localization, and cell type.


Source of the Dataset: This dataset is a large collection of multi-sources dermatoscopic
images of pigmented lesions from different populations, acquired and stored by
different modalities. The final dataset consists of 10015 dermatoscopic images
which can serve as a training set for our project. The URL for the data is as
follows: https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000 



 



Data Pre-processing



Image data pre-processing can be used to increase model
performance and reduce generalization error, while improving a fit model's
prediction performance. 




The next step was to reduce the dimension of the images from
a four-dimensional array to a two-dimensional array. This step is very
important as this will help us train the supervised ML models like SVM and
Random Forest. Both these classifiers require a 2-D array.





Further we have also normalized the array by dividing it by
255. This will help us to transform the features to be on a similar scale. This
improves the performance and training stability of the model.



For the data pre-processing of HAM10000 metadata.csv file,
the most important step performed is converting the categorical column ‘dx’,
which contains the type of skin cancer that is shown in the image, into
numerical values. Since there are seven types of skin cancer, the numerical
values range from 1 to 7. 



------------------------------------------------------------------------------------


Support Vector Machine



The basic idea of the support vector machine is to first map
the original data space transform to a high-dimensional feature space by flying
nonlinear transformation, and then find the optimal linear classification
surface in this new space. This nonlinear transformation is achieved by
defining an appropriate inner product function. The support vector machine
algorithm seeks a hyperplane in an N-dimensional space (N — the number of
features) that distinguishes between data points. There are several hyperplanes
that might be used to split the two groups of data points. Our goal is to
discover a plane with the greatest margin, or the greatest distance between
data points from both classes. Maximizing the margin distance gives some
reinforcement, allowing subsequent data points to be categorized with more certainty.






Hyperplanes are decision boundaries that aid in the
classification of data items. Data points on either side of the hyperplane
might belong to distinct classes. Furthermore, the size of the hyperplane is
determined by the number of features. When the number of input features is two,
the hyperplane is just a line. When the number of input characteristics reaches
three, the hyperplane transforms into a two-dimensional plane. When the number
of characteristics exceeds three, it becomes impossible to imagine.



 



Random Forest



A forest is the collection of trees; a random forest is the
collection of classification trees. Classification tree, sometimes also called
as decision tree, is the construction of a tree which consists of the members
of the class variable on its leaf nodes and the entities of other dependent
variables reside on the intermediate nodes. Class variables are also called as
decision variables or predictor variables, which may comprise, for example, yes/no
decision to predict a disease or loan approval, spam/no spam in the case of
emails, good/bad/moderate for the product qualities, 0-9 for handwritten digits
in the case pattern recognition, etc. Random forests develop many
classification trees, and to add a new classification tree to the forest, add
it down to the each of the trees in the forest. Each tree provides its
classification, and we consider it as its vote for that class. The forest
considers the classification receiving the most votes from all the trees in the
forest.



 



CNN



Convolutional neural networks are deep learning algorithms
that take input images and convolves it with filters or kernels to extract
features. A NxN image is convolved with a fxf filter, and this convolution
operation learns the same feature on the entire image. The window slides after
each operation and the features are learnt by the feature maps. The feature
maps capture the local receptive field of the image and work with shared.  



 



 



 


[Project Report](https://github.com/VANSHIKA-N/SkinCancerDetection/files/11365293/Final_Report.pdf)
