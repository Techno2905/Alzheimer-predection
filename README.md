# Alzheimer-predection
Alzheimer predection using CNN model
TABLE OF CONTENTS

1.	Abstract……………………………………………
2.	Introduction…………………………………
3.	Alzheimer’s……………………………………
4.	Methodology……………………………………
5.	Results………………………………………………

ABSTRACT

The Alzheimer’s disease is a progressive disorder of the brain that causes the death of brain cells due to shrinking of the brain. It also is the leading cause for dementia, which causes a considerable decline in the ability to think, behave and to socialize which can affect the ability of a person to function independently. Image processing is widely used for the detection of Alzheimer’s using the mri scans of the brain.  Early diagnosis of AD is essential for the progress of more prevailing treatments. Detecting Alzheimer’s is a difficult and time consuming task, but requires brain imaging report and human expertise. Needless to say, this conventional approach to detect Alzheimer’s is costly and often error prone.
Early detection with the possible use of machine learning algorithms and image processing can help in easier and early detection of alzheimer’s and therefore can help the medical faculty to come up with the best treatment plan in hope of reducing the mortality rate caused due to Alzheimer’s.

INTRODUCTION 

Brain is the primary organ of the human body. The diseases that affect brain is very crucial to handle since mostly once changes occur it is irreversible in extreme cases. Dementia means the loss of cognitive functional thinking. Alzheimer’s is most common cause of Dementia. Alzheimer’s first appear in their mid-60’s.It is estimated that more than 5.5 million people are having Alzheimer’s .The Alzheimer’s disease symptoms include memory loss, language problem, behavior changes. . The non-memory aspect symptoms are difficulty in word finding, vision issue, impaired reasoning and impaired judgement. The biological sign are brain images, cerebrospinal fluid and blood. The Alzheimer’s disease can be classified As Mild Alzheimer’s disease, moderate Alzheimer’s disease and severe Alzheimer’s. 
Machine learning is used to interpret and analyze data. Furthermore it can classify patterns and model data. It permits decisions to be made that could not be made generally utilizing routine systems while sparing time and endeavors. Machine learning methodologies have been extensively used for computer-aided diagnosis in medical image formation mining and retrieval with wide variety of other applications especially in detection and classifications of brain disease using CRT images and x-rays. It has just been generally late that AD specialists have endeavored to apply machine learning towards AD prediction.

ALZHEIMER’S

Alzheimer’s disease (AD) is a degenerative disorder of the brain that leads to memory loss. It is the most common form of dementia, caused by the build-up of beta amyloid plaques in the brain. The plaques and tangles are some of the main features of the disease. As the number of Plaques and tangles increases, the healthy neurons begin to function less effectively and gradually lose their ability to communicate and finally die which results in overall shrinkage of the brain tissues. The death of neurons particularly in the hippocampus restricts the ability to form new memories. The hippocampus is the first region in the brain which gets affected. It is the region in the brain that is responsible in forming memories and serves as a relay structure between the brain and the body. 
As Alzheimer’s is a progressive and irreversible disease it progresses gradually following a distinct pattern of brain damage and can last for decades. The disease progresses slowly into three main stages namely mild, moderate and severe, where each stage has its own symptoms and challenges. The mild stage generally lasts for about an average of 2 to 4 years in which a person may function independently but may have memory lapses. In the moderate stage a person may require assistance in carrying out day to day activities and may experience increased difficulty with memory. This stage is probably the longest stage of the disease and may last for a duration of about 2 to 10 years.
There are degrees of severity in Alzheimer.
1.	Very mildly demented : This is the stage where patient starts to forget where they put their stuff, other people's names recently, etc. It is hard to detect through cognitive ability test.
2.	Mildly demented : This is the stage where patients don't remember the words, can't find their way to the destination, loss of focus and work-abilities. This is also the stage where patients even forget that they are losing memory. From this stage, with cognitive testing, it can be found.
3.	Moderately demented : Starts to forget the recent activities, important old histories, have hard time calculating the budget, hard to go outside alone, and loss of empathy.

METHODOLOGY

DATASETS AND SOFTWARES
A.	Alzheimer MRI Preprocessed Dataset (128x128)
•	The data is collected from several websites/ hospitals/ public repositories.
•	The dataset consists of pre processed MRI images.
•	All the images are resized into 128x128 pixels.
•	The dataset has four classes of images.
•	The dataset consists of a total of 6400 images
Class 1: mild demented (896 images)
Class 2: moderate demented (64 images)
Class 3: non demented (3200 images)
Class 4: very mild demented (2240 images)

B.Softwares
•	KAGGLE: Kaggle is an online community platform for data scientists and machine learning enthusiasts. Kaggle allows users to collaborate with other users, find and publish datasets, use GPU integrated notebooks, and compete with other data scientists to solve data science challenges.
•	PYTHON: PYTHON is a general-purpose programming language that runs on almost all system architectures and can be used for a wide range of applications in different fields, from web development to machine learning. Python is used to organize and clean data. It is considered as one of the best programming languages to do it. Additionally, machine learning with Python simplifies the data analysis with the use of algorithms.
•	VISUAL STUDIO: Visual Studio is an integrated development environment (IDE) from Microsoft. It is used to develop computer programs including websites, web apps, web services and mobile apps. Visual Studio uses Microsoft software development platforms such as Windows API, Windows Forms, Windows Presentation Foundation, Windows Store and Microsoft Silverlight. It can produce both native code and managed code. 



![image](https://user-images.githubusercontent.com/78484243/218210460-1e6102a7-f01a-4ef9-b5ed-67b2d9108d18.png)

    Block diagram


The main aim of this project is to design/ develop an accurate framework or architecture for the classification of Alzheimer’s disease.
1.	The dataset images are given as input to the CNN model.
2.	Building the model: We rescale the images to fit between [0,1] then for each convolutional layer we can see that the size increase 16-32-64 the parameter 3 is the kernel size often it's 3 but we can see 5 too we specify the padding as same this mean when the convolution occurs we put all around the image 0 pixels because when you are making convolution the kernel have to be in the center of all the pixels that it see, if we do not add padding it cannot convolute the edges so we will loose some information,The max pooling have a size of 2 by 2 matrix it parse the images and get the maximum value between 4 pixel and so on.... at the end we add a dropout layer to avoid overfit this will off some neurons randomly then we add a flatten layer to put all this in one dimensional array, the activation is relu except for the last layer that have to return us a probability of belonging to each class so the last layer have to have as neurons the number of classes.
3.	Model used: 2D convolution model- Keras Conv2D is a 2D Convolution Layer, this layer creates a convolution kernel that is wind with layers input which helps produce a tensor of outputs.
4.	We train the model upto 5 epochs.
5.	We plot the accuracy of the model.     
    ![image](https://user-images.githubusercontent.com/78484243/218210383-05c830be-e407-4254-888f-028d5dfc7232.png)

		Plot of accuracy.
    
6.	We test the model by providing an input of 25 random images from the dataset.
7.	It is observed that the trained model classifies the images into their right classifications with an accuracy of 90-92%.



RESULTS

After completion of training, the model is tested for its prediction. This is done by providing 25 random images from the dataset to check the accuracy of prediction of the trained model.
![image](https://user-images.githubusercontent.com/78484243/218210316-f1ad0d6f-8dab-4a61-825c-8279ad6cff87.png)


