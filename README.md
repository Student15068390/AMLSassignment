# Assignment Overview

### Intro
Welcome to the Applied Machine Learning Systems Assignment!

During the last couple of years, Artificial Neural Networks (ANN) have acquired major attention due to breakthroughs in a variety of fields such as voice recognition, natural language processing, and computer vision. Thanks to statistical methods, the capabilities behind these networks are impressive; without any prior knowledge about large amounts of data, they can estimate patterns and formulate underlying functions.

We have been presented with a dataset of 5000 labeled images which was specifically designed for this challenge. It consists of pre-processed subsets from the following datasets: CelebFaces Attributes Dataset – face images of celebrities; and Cartoon Set dataset– face images of cartoons. Moreover, we must note that some noisy images have been added to the dataset, more specifically images of natural backgrounds, which are expected to be removed before processing our data.

The aim of this repository is to demonstrate how to successfully clean our dataset and correctly classify the images contained within it. 

### Repository composition

The repository is composed of the following folders:
- Binary Tasks: 
Containing the codes of all attempts to solve the binary classification challenge

>**FinalModels_Inception_CleanData** is the most important one. It contains the codes which allowed us to solve our problem and create the required CSV files.

>**SVM_Implementation** contains the codes of the SVM Implementations to the binary tasks. These are considered as a benchmark to the other models. 

>**WithNoise_InceptionModel** contains the same codes as the FinalModels file above, however these were processed with Noise included in the dataset.

- CSV_Results:
Where to find all the csv files requested.

- Multiclass_Task:
Contains the code of the multiclass task for Hair_Color recognition both WITH and WITHOUT Noise. 

- Noise_Cleaner:
 Contains the code for the noise cleaning step of the assignment. 

- Supplementary_Work
Contains codes of practice work carried prior to tackling the challenge, as well as other attempts to solve the challenge by using different classifiers such as the Haar or LBP classifiers. 

# Install and Run

In order to run the code, you will need to do the following:

1. Install Anaconda
2. Instal Jupyter Notebook
3. Open Anaconda Prompt (Command Terminal)
4. Create a python 3.6 virtual environment called *py36*
> conda create --py36 py36 python=3.6
5. Verify environment is created
> conda info -e
6. Activate the environment
> conda activate py36
7. Install all required libraries
> pip install ...
8. Verify that all libraries are installed
> conda list
9. Open Jupyter Notebook
> jupyter notebook
10. Download from GitHub and upload files on jupyter notebook
11. Check the important parameters section below to adjust directories and other details to your computer
12. Run the code

# Important Parameters

### In AMLS_NoiseCleaner

Please make sure to change the right directory according to the path on your computer. 
If you decide to change any of the folders name, please do change the name throughout the code as well. 

_basepath = "C://Users/xxxxx/Desktop/"          
class1 = os.listdir(basepath + "Person/")    
class2 = os.listdir(basepath + "Background/")
class3 = os.listdir(basepath + "test/")_

Another change to make in order to run the code is at the end when storing the noisy pictures in a new document. 
_img = testimgs[1].split('/')
['C:', '', 'Users', 'karim', 'Desktop', 'Test', '10.png']_

As the directory that I run the code on has the structure shown above, in the code I choose to split and store the sixth value, which is the value of the filename. When changing the directory, please make sure to change the number accordingly. 

_noise_images = []_

_noise_images.append(image[6])_ <--------

### In AMLS_ all classification tasks

Please make sure to input the right directory on your computer prior to running the code.
This can be done at the start of the code in the following lines:

_main_folder = 'C://Users/xxxxxx/Desktop/'_

_images_folder = main_folder +'clean_AMLSdataset_mediumset/'_








