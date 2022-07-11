# Nano33 BLE Sense
In this Project, we want to deploy a music classifcation model on the Nano33.
The first version of this model, classifies songs in three categories: 1.Classic 2.Pop 3.Metal
The GTZAN dataset used for training this model

To test and use mode, we can record the song with Nano33, Mobile phone or upload a file from computer.






First step was installing Edge Impulse CLI and other drivers and preparing software configuration requirements.
Then, we created a project in the edge impulse website, and did these steps in order:
1.	Data acquisition: in this step we have to upload training and testing dataset.
The data we used, was from GTZAN data source, which included 100 songs for each genre.
2.	Impulse design: This step itself, includes three sub steps:
A)	Create Impulse: In this sub step, we can set and configure DSP block and ….
B)	Audio: In this sub step we normalized dataset.
C)	NN Classifier: In this step, we set and configure neural network architecture, like learning rate, number of layers, adding noise to dataset, dropout value and …
This step is very important and each parameter can affect result significantly.

 
 
 
 
3.	EON Tuner: This step is auto ML and suggests models to increase accuracy, but we should consider overfitting in this step, in very high accuracies, model is probably overfitted.
4.	Live classification: This step is to test trained model, with uploaded data or recorded data.
After these steps, our model had 96% accuracy! But after testing recorded samples with mobile phone and Nano 33, results weren’t desirable. It seemed the model overfitted and couldn’t work with new recorded data, but worked well with music files. Therefore we thought maybe the problem was the noise in the recorded samples, so we increased data drop-out data and added noise.
Accuracy decreased, but recorded samples with mobile and Nano33 worked better.
