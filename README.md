This project is used for recognising the way different numbers are written and identifying what number it is.
It's used in banks to check if the account number is right by 
comparing each number written to all the different numbers with different fonts stored in the program.
This code uses a database called minst which stores almost 7000 hand written numbers from 0 to 9.
Out of those 7000,6000 are used for training the program and the rest 1000 is for testing it.
After the first part of importing all the libraries and assigning the variables for traning the data set,
keras is used.
Keras is a module from tensorflow library used to train the model where in the model needs to be trained in layers to understand each component precisely.
It acts like many neurons combined to make the full model.
This method is called neural networking.
The layers(present inside keras) used in this code are:-
  1. Conv2D - is the top and the only visible layer where it is used to remove special effects from a 2D image like an imge of 9 means the layer will extract all the points
where it is curved and flat.
It will stores the features which it found from the specific image.
  2. MaxPooling2D - is the hidden layer(it does work but is not visible outside to the users) which is used to downsample the features found by the Conv2D layer,
to save memory and make it faster to access.
  4. Dense - also a hidden layer and is the last layer used to train the model properly.
It is used to understand complex structures in the hand written image and store the features identified.
These complex and deep structures,only the dense layer can find.
  3. Flatten - in-between the maxpooling and dense is this hidden layer.
Every time each and every image will first go through conv2d and max pooling.
After the first 2 layers are done only then it moves to the last layer,flatten and the process repeats for the next image.
The  3rd layer is for comparing the results and then converting the features found by the dense layer to a lower resolution.
Mainly the dense layer retrieves data in 3d form so the flatten layer basically flattens it(as the name suggests) into 1d format.
After all these layers are down and the model has processed all the data thruogh the layers,it is compiled and a summary is printed.
The summary is used to see what has the file size changed to for each layer.
It also shows the total number of models present,how many were a success and actually
got trained and how many unfortunately remanined untrained.
Then the trained model is tested for how much is the accurary and loss by inputing the 1000 images stored for testing.
The accuracy is checked,if satisfied then it moves ahead,but if accurary is less than 90 then the process is restarted and if needed then made some changes
to the trained model.Once trained again it is tested till it has satisfied the criteria.
Once all the testing is done then the final step,
a random image is provided from the tested image,and is asked to predict the number.
The modelling process starts and matplotlib library is used to plot a graph with only axis and then show the image given and the prediction it showed.
This is how this program can be used to recognise different fonts and identify the accurate number.
