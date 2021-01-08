# Down-Boy
Student Name: Gavin Soady Student ID: 2009115411

Monty our pet dog knows he’s not allowed on the couch, but will chance his paw every now again when we are not looking. Despite his sneaky demeanor he is very obedient and will get down the second he’s told.

So my project proposal is called Down-boy. Using the raspberry pi camera to track Monty's movement if/when he gets up on the couch the Application should do a number of things.

Detect dog "object" on the couch(camera set-up to only have couch in view) using tensor flow and openvino.

Take a picture of the rule breaker.

Upload to firebase. store and feed lattest image to web application

send a sms to my phone via twilio with link to down-boy web app.

Future Development:

Broadcast a prerecorded message to a smart speaker to tell the mutineer to get down.

Wrap web application in android app via phone gap build.

If second infringement is caught within a determined period of time, send a picture to a phone application.

The phone app will allow the user to Broadcast a message to the smart speaker, request an up to date picture and option to connect via live stream.

Disconnect from live stream and reset procedure. 

Tools, Technologies and Equipment 
  
  Hardware:
 
 Raspberry Pi
 
 Raspberry Pi Camera
 
 Google home mini smart speaker
 
 Mobile phone

Software for Raspberry Pi:
  
  Python
  
  Raspberry Pi OS
  
  picamera
  
  tensor flow 
  
  twilio
  
  firebase

Software for Mobile Application:
  
  HTML5/CSS3/JavaScript
  
  Java
  
  Play Framework(This may have to be deployed on a separate website
  
  Phone Gap/Ionic

  Installation instructions:

Dependencies: 

Set up Firebase account
  
  https://tutors-svelte.netlify.app/#/lab/wit-hdip-comp-sci-2020-computer-systems.netlify.app/topic-10-week10/unit-2/book-a
  
Create Glitch app:
  
  https://tutors-svelte.netlify.app/#/lab/wit-hdip-comp-sci-2020-computer-systems.netlify.app/topic-10-week10/unit-2/book-a/04
  
Install tensorflow:
  
  pip3 install tensorflow
  
  sudo apt-get install libatlas-base-dev
  
  sudo pip3 install pillow lxml jupyter matplotlib cython
  
  sudo apt-get install python-tk
 
Install OpenCV
  
  sudo apt-get install libjpeg-dev libtiff5-dev libjasper-dev libpng12-dev
  
  sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
  
  sudo apt-get install libxvidcore-dev libx264-dev
  
  sudo apt-get install qt4-dev-tools libatlas-base-dev
  
  sudo pip3 install opencv-python
  
Install Protobuf
  sudo apt-get install protobuf-compiler
  
Set Up application
  mkdir Down-boy
  cd Down-boy 
  git clone --depth 1 https://github.com/Gavin-Soady/IOTAPP.git
  
  Natigate to:
    sudo nano ~/.bashrc
 
 Enter at the end:
    export PYTHONPATH=$PYTHONPATH:/home/pi/Down-boy/object_detection
  
  Navigate back to Down-boy directory
    protoc object_detection/protos/*.proto --python_out=.
  
  Navigate back to Down-boy/object_detection directory
    move storeFileFb.py here
    move serviceAccountKey.json here
  
  Download tensor flow models:
    wget http://download.tensorflow.org/models/object_detection/ssdlite_mobilenet_v2_coco_2018_05_09.tar.gz
  
  Unpack with:
    tar -xzvf ssdlite_mobilenet_v2_coco_2018_05_09.tar.gz
  
  Set up twillio account 
    https://www.twilio.com/docs/sms/quickstart/python
  
  Set Envirnment variables:
    https://www.twilio.com/blog/2017/01/how-to-set-environment-variables.html
  
  Run Script:
   Python Down-Boy.py
