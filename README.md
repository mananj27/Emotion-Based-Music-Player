# Emotion-Based-Music-Player
Introduction - 
Music plays an important role in a person’s life as it is very therapeutic and is a source of entertainment. Music is always known to alter the mood of an individual.
Human expression plays a vital role in determining the current state and mood of an individual, it helps in extracting and understanding the emotion.
Taking these two aspects and blending them together our project deals with detecting emotion of an individual through facial expression and recommending music according to the mood detected. 

Problem Statment - 
It is often confusing for a person to decide which music he/she wants to listen from a massive collection of existing options.
Due to the troublesome workloads in songs selection, most people will choose to randomly play the songs in the playlist. 
As a result, some of the songs might get selected which might not be matching the users’ current emotion.
The user has got to face the task of manually browsing the playlist of songs and choose songs supported their current mood and behavior while busy working in his/her task.

Proposed Solution - 
Capturing and recognizing the emotion being voiced by a person and displaying appropriate songs matching one’s mood and can increasingly calm the mind of a user and overall end up giving a pleasing effect.
The main objective of our music recommendation system is to provide suggestions to the users that fit the user’s preferences, so the person doesn't need to stop working again and again to change the songs.

Face Detection - 
The system will capture the real time image of the user and proceed it further to the model.
We have used Tenser Flow, Keras and NumPy to make  and load the model and modules like MediaPipe and Holistic for detecting facial emotions and hand moments of the user.
MediaPipe is an ultra fast face detection solution which comes with 6 landmarks and multi face support to capture each minute detail of the face.

Mood Detection - 
Different facial landmarks can be detected using the Holistic from the MediaPipe. We have used a model which is trained with our own dataset which will comprise of numerous images where each image belongs to one of the classes i.e., Anger, Happy, Sad, Surprise and Neutral.
Further the model will send the emotion detected to the model for songs recommendation.

Music Recommendation - 
The detected facial emotion will be used as a keyword to recommend songs to the users.
The webpage will redirect the users to their desired music players (i.e., YouTube, Spotify, etc.)
This application will ask the user for their desired language for the song which will be recommended to him/her.

Dataset - 
 We have created the model with FER2013 Dataset from Kaggle and with our own dataset.
The training set consists of 28,709 examples of  grayscale images of faces.
The faces have been automatically registered so that the face is centered and occupies about the same amount of space in each image.
The dataset consists face images for happy, disgust, angry, fear, sad, surprise and neutral expressions.
The current accuracy for the model with FER2013 dataset is 78% while using our dataset got us an accuracy of about 65%.

Libraries - 
Streamlit : Streamlit turns data scripts into shareable web apps in minutes without any front‑end experience required.
AV : PyAV is for direct and precise access to your media via containers, streams, packets, codecs, and frames. It exposes a few transformations of that data, and helps you get your data to/from other packages (e.g. Numpy and Pillow).
OpenCV :It is used to process images and videos to identify objects, faces, or even handwriting of a human. When it integrated with various libraries, such as NumPy, python can process the OpenCV array structure for analysis.
NumPy : NumPy is a Python library used for working with arrays. NumPy aims to provide an array object that is up to 50x faster than traditional Python lists.
MediaPipe : It is a cross-platform library developed by Google that provides amazing ready-to-use ML solutions for computer vision tasks.
Keras : It is an open-source software library that provides a Python interface for artificial neural networks. Keras acts as an interface for the TensorFlow library.
TensorFlow : It is used to implement best practices for data automation, model tracking, performance monitoring, and model retraining. 
