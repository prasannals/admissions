# Projects

## Shoulder Press Rep Counter

![shoulder_press_gif](https://media.giphy.com/media/LpRhZB7VqUYRNe3FSS/giphy.gif)

Full Video Demo - https://youtu.be/s1Ac4gcfNO4

<strong>Functionality</strong>
* Keeps track of the number of repetitions performed on the shoulder press workout.
* Can be extended to inform user of bad form during workout.

<strong>Under the Hood</strong>
* Tracks the dumbbells as well as the persons face.
* If an imaginary line, say L1, is drawn from the center of the persons face to the center of the dumbbell and another imaginary line, say L2, is drawn from the center of the persons face vertically to the top of the screen, the algorithm calculates the angle between L1 and L2 for both the dumbells.
* Certain angle thresholds are defined to track the reps. Currently 35 and 65 degrees but more research needs to be done to find the optimal angle. Currently, if both angles made by dumbbells go below 35 degrees and then above 65 degrees, the number of reps is increased by 1.

## Spot ( Play/Pause Video using gestures )

![](https://media.giphy.com/media/37sn0jEnY5nIjYZyTz/giphy.gif)

Full Video Demo - https://www.youtube.com/watch?v=1SIyaon6S50

<strong>Functionality</strong>
* Play/Pause video on VLC Media Player when the hand is raised up (with fingers spread out and palm facing towards the camera)
* Swipe hand left/right to skip backward/forward in the video (in progress)

<strong>Under the Hood</strong>
* Uses a regular web camera to capture the video.
* Hand Detection is done using <a href="https://arxiv.org/pdf/1512.02325.pdf">SSD</a>.
* PyTorch is used for implementation. PyAutoGUI is for GUI automation (play/pause) video.

## Sentinel - Face Detection, Face Recognition, Person Detection

![](https://media.giphy.com/media/Lkm1Fox6uM4iNx8CE7/giphy.gif)

Full Video Demo - https://youtu.be/Vh9dNs2pxz8 (face recognition model trained on my face(Prasanna) and my cousin's face (Tejas) but not on my moms face (and hence says "a person has arrived") )

<strong>Functionality</strong>
* Face detection and recognition system. Upon detecting a face, sends a mail with persons pic and name attached.
* If it isn't trained on some face and is therefore unable to recognize a face, it can still the presence of a person and a face and sends a mail saying that some person has arrived (with the pic of the person attached to the mail)
* Works with any video stream (IP Camera, online video stream, video recording etc. )

<strong>Under the Hood</strong>
* Uses SSD for person detection. 
* Uses Haar Cascade for Face Detection. 
* Uses resnet-34 for face recognition.
* To denoise and enhance the face detection, face detection is applied on the cropped image of the detected person once a person is detected.
* Prediction is made after considering multiple frames leading to more robust face recognition.

## Image Source

<img src="https://i.imgur.com/9xZtAPU.png" width="250" /> <img src="https://i.imgur.com/P1tdTeK.png" width="250" /> <img src="https://i.imgur.com/cpQOZ9K.png" width="250" />

<img src="https://i.imgur.com/0tP88NG.png" width="250" /> <img src="https://i.imgur.com/FXDZJT0.png" width="250" /> <img src="https://i.imgur.com/FOVTaYw.png" width="250" />

Prediction Demo - https://youtu.be/Fe8uBVMcH8U

Expo Link (download the <a href="https://play.google.com/store/apps/details?id=host.exp.exponent">Expo app on Play Store</a> to try Image Source) - https://expo.io/@prasannals/image-source

Usage instructions and server code - https://github.com/prasannals/image_source_server

Image Source App Code - https://github.com/prasannals/image-source

<strong>Functionality</strong>
* App is aimed at helping computer vision practitioners collect and send data to their predictive ML models easily.
* Users can click pics, categorize and store the pics in folders within the app.
* Send all the pics to the server with one click.
* Prediction can be done using existing the phones camera. The image will be sent to server and the prediction will be displayed.
* Can remotely signal the ML model to train itself on the data.
* In the backend, the user of the framework has to implement "train" and "predict" methods and has to pass it into the framework which then handles setting up server, receiving images, storing images, delegating requests to appropriate methods and returning prediction responses.


<strong>Under the Hood</strong>
* Created using <a href="https://facebook.github.io/react-native/">React Native</a> (apps are written in JavaScript) and the <a href="https://expo.io/">Expo</a> framework. 
* Backend is written in Python. Uses Flask server.

## Echo

![Imgur](https://i.imgur.com/lL0j0hH.png)

YouTube link to Demo and Explanation - https://www.youtube.com/watch?v=KsHb4U13h0A

Code and JAR Files (to execute the project) - https://github.com/prasannals/Echo

<strong>Functionality</strong>

* Echo extracts features from a graph and produces an audio which is representative of that graph.
* This can be applied to any graph, but is intended to be used with social network graphs. 
* There are two audio "channels" that you may listen to -
  1. Friend Cluster - Plays a sound representative of any node "n" based on how closely knit (based on clustering coefficient) his network is.
  2. Similarity - Given that the observer is a node "n1", it plays a sound representative of any node "n2" based on how similar n1 and n2's network is.
* Refer the <a href="https://drive.google.com/file/d/0B5mK3-MF9-FJcEpjeVE5NERXRXc/view?usp=sharing">paper</a> I've written on this topic for an in depth explanation.

<strong>Under the Hood</strong>
* Implementation is done using Java.
* Graph visualization is done using JUNG library and audio is produced using Beads library for Java.

## Text Templates (available on Play Store, 15k+ downloads)

<img src="https://i.imgur.com/Ni8CS87.png" width=270 /> <img src="https://i.imgur.com/6j5g8ka.png" width=270 /> <img src="https://i.imgur.com/ufWcDBG.png" width=270 />

<strong>Functionality</strong>
* Lets the user save frequently used text. The user can later send the text to any application on their phone with just a click of a button.
* Check <a href="https://play.google.com/store/apps/details?id=texttemp.ps.texttemplates">Play Store</a> for more information, images, reviews and of course, do give it a try!

<strong>Under the Hood</strong>
* Created using Java (native android).

## Nakshatra Creations (available on Play Store and App Store(soon))

<img src="https://i.imgur.com/UGtD8kk.png" width=300 /> <img src="https://i.imgur.com/i1SJoOm.png" width=300 />

<strong>Functionality</strong>
* Android and iOS app for Nakshatra Creations, a non profit organization focused on entertainment. 
* App has a list of videos which is dynamically retrieved from backend and shown to the user along with a thumbnail. 
* Opens the YouTube app with selected video upon clicking the video. 
* Push Notifications can be send to notify users when a new video is released.
* Check <a href="https://play.google.com/store/apps/details?id=org.nakshatracreations.app">Play Store</a> for more information, images and to try it out! Check Nakshatra Creations <a href="http://nakshatracreations.org/index.html">website</a> for more info about the organization.

<strong>Under the Hood</strong>
* Built using React Native and Firebase.

## Animated List

Full Demo - https://www.youtube.com/watch?v=OzzlP0dJIzQ

Code - https://github.com/prasannals/AnimatedList

<strong>Functionality</strong>
* Language and interpreter for the language to help visualize lists.
* <strong>The language</strong>
  1. add **element**
  2. delete **index**
  3. highlight **index**
  4. set **index**,**element**
  5. swap **index**,**index**
* Compile and feed the program with the file with each instuction on a separate line.
* Output

![](https://media.giphy.com/media/4N99ISJvzWsOpAQlfq/giphy.gif)

<strong>Under the Hood</strong>
* Built using C++
* Uses OpenGL for visualization.

## Find Movies

![](https://media.giphy.com/media/V2VpvnZGDw88s7WfnP/giphy.gif)

App Demo - https://www.youtube.com/watch?v=Qdl_GgNQww0

Code - https://github.com/prasannals/FindMovies

* Helps in finding popular/highest rated movies. 
* Has an infinite list of movies which will be sorted according to popularity/ratings. 
* Clicking on any movie gives a short description of the movie, poster, ratings, links to trailers(launches YouTube app on click) and user reviews. 
* User will also be able to save their favorite movies for viewing it offline(data will be stored in a SQLite database locally).
* Built using Java (native android).

## Earthquake Map

![](https://media.giphy.com/media/5sYtqIVY4bKkDxWtz6/giphy.gif)

<strong>Functionality</strong>
* Displays a map on which the past week's earthquakes (data is retrieved online from <a href="https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/2.5_week.atom">here</a>)  are shown using markers.
* Allows for zoom into/out of map and scrolling the map using the mouse.
* On clicking a city, earthquakes close to that city will be displayed
  <img src="https://i.imgur.com/rp15LOa.png" width="500" />
* On clicking an earthquake, more information about that earthquake will be displayed
  <img src="https://i.imgur.com/kAK86Ov.png" width="500" />
* Done as a part of <a href="https://www.coursera.org/learn/object-oriented-java?specialization=java-object-oriented">Object Oriented Java Programming</a> course at Coursera.

<strong>Under The Hood</strong>
* Built using Processing extension for Java and UnfoldingMaps for Processing. The map is provided by GoogleMapProvider.

## Smart Text Editor

![](https://media.giphy.com/media/Vc6AYA8HkSVBXcf4AM/giphy.gif)

Demo - https://www.youtube.com/watch?v=bJnn4mde3lg

* Auto suggest feature while typing(using Trie data structure).
* Checks for spelling mistakes when spell check is turned on.
* Scores the readability of a text using Flesch Score.
* Generates text using Markov Text Generation.
* Done as a part of <a href="https://www.coursera.org/learn/data-structures-optimizing-performance?specialization=java-object-oriented">Data Structures and Performance</a> course at Coursera.

## Routing on Maps

![](https://media.giphy.com/media/TGcHK61jlNEKbowYUF/giphy.gif)

Demo - https://www.youtube.com/watch?v=qJ92qRCitk0

* Finds and displays the shortest path between two intersections.
* Option to choose from BFS, Dijkstra's and A* algorithm.
* Done as a part of <a href="https://www.coursera.org/learn/advanced-data-structures?specialization=java-object-oriented">Advanced Data Structures</a> course at Coursera.

## Chopper

#### Light Theme
![GamePlay](https://media.giphy.com/media/cI4tpm7N0s5C3s8Pju/giphy.gif)

#### Dark Theme
![GamePlay](https://media.giphy.com/media/pcKOnyeZiMvguEzJjZ/giphy.gif)

Code : https://github.com/prasannals/Chopper

Link to play game : https://prasannals.github.io/Chopper/

* The classic Chopper game created using <a href="http://www.purescript.org/">PureScript</a> and Presto DOM (<a href="https://juspay.in/">Juspay's</a> framework). 
* Press SPACE to elevate the helicopter and avoid obstacles.
* <strong>Purpose of creating this project was to learn purely functional programming (using PureScript)</strong>
* Check https://github.com/prasannals/SimonSays for another game created with the same intention of getting used to pure functional languages.

## Machine Learning Projects done as a part of Machine Learning courses at Coursera

1. Boston Housing Price Prediction (Polynomial Regression, Ridge Regression, Lasso Regression)
2. Amazon Baby Product Review Sentiment Analysis (Logistic Regression, TFIDF)
3. MNIST Digit Classification (Neural Networks, Logistic Regression, CNN)
4. Email Spam Classification (SVM)
5. Image Compression (k-means)
6. Movie Recommendation (MovieLens dataset, using Collaborative Filtering)
