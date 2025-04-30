<p align="center">
  <img src="https://github.com/JoanEstopCepero/StarGazer/blob/main/img/StarGazer.gif" width="500" />
</p>

# STARGAZER

__Star Gazer__  is an interactive robotic system powered by a Raspberry Pi, designed to help users visualize stars, constellations, and planets in real time. Equipped with a laser pointer, the robot can physically point to celestial objects visible from the user's current location and time, creating a hands-on stargazing experience.

## Features

- **Laser-guided pointing** of visible stars, constellations, and planets based on geolocation and time.
- **Dual control modes**: interact with the robot via a mobile application or voice commands.
- **Photo analysis**: upload a photo via the app or capture one using the robot’s built-in camera. StarGazer will identify and label the visible constellations and stars directly on the image.
- **Educational and engaging**: ideal for learning about astronomy in a tangible, user-friendly way.

To test the accuracy and functionality of the prototype—especially given the limited power of the laser—we built a custom observation dome. Inside this dome, we hand-drew the constellations to simulate the night sky. We used the Stellarium application to obtain the correct orientation angles for each star, allowing us to position them as they would appear in real celestial coordinates. This setup allowed us to validate that the robot could accurately point to the intended stars and constellations within a controlled environment.

Whether you're just getting into astronomy or simply fascinated by the night sky, StarGazer is here to help you spot and learn about the stars above. The idea behind this robot is to make it easier and more fun for anyone interested in the cosmos to actually see and understand the stars, constellations, and planets in the sky.

# TABLE OF CONTENTS
- [Hardware Requirements](https://github.com/JoanEstopCepero/StarGazer/tree/main?tab=readme-ov-file#hardware-requirements)
- [Software Requirements](https://github.com/JoanEstopCepero/StarGazer/tree/main?tab=readme-ov-file#software-requirements)
- [Documentation](https://github.com/JoanEstopCepero/StarGazer/tree/main?tab=readme-ov-file#documentation)
- [Project Module](https://github.com/JoanEstopCepero/StarGazer/tree/main?tab=readme-ov-file#project-module)
- [Hardware Architecture](https://github.com/JoanEstopCepero/StarGazer/tree/main?tab=readme-ov-file#hardware-architecture)
- [Algorithms](https://github.com/JoanEstopCepero/StarGazer/blob/main/README.md#algorithms)
- [Images](https://github.com/JoanEstopCepero/StarGazer/tree/main?tab=readme-ov-file#images)
- [3D](https://github.com/JoanEstopCepero/StarGazer/tree/main?tab=readme-ov-file#3d)
- [Video](https://github.com/JoanEstopCepero/StarGazer/tree/main?tab=readme-ov-file#video)
- [References](https://github.com/JoanEstopCepero/StarGazer/tree/main?tab=readme-ov-file#references)
- [Authors](https://github.com/JoanEstopCepero/StarGazer/tree/main?tab=readme-ov-file#authors)

# Hardware Requirements
- Raspberry Pi 3b
- Raspberry Cam
- x2 Stepper Motor 28BYJ-48
- x2 Driver ULN2003
- Power Bank
- Laser

# Software Requirements
For development:
- Fully developed in Python

For running the code:
- flet
- firebase_admin
- credentials
- firestore
- storage
- translate_v2
- os
- texttospeech
- io
- pygame
- speech_recognition
- threading
- re
- json
- pyrebase
- requests
- Nominatim
- EarthLocation
- AltAz
- get_sun
- get_moon
- get_constellation
- SkyCoord
- Time
- units
- numpy
- datetime
- pytz
- cv2
- matplotlib.pyplot
- combinations
- KDTree
- os
- tempfile
- socket
- Image
- datetime
- timedelta

# Documentation
Software:
- [flet](https://flet.dev/)
- [firebase_admin](https://firebase.google.com/docs/reference/admin/python/firebase_admin)
- [credentials](https://firebase.google.com/docs/admin/setup?hl=es-419)
- [firestore](https://stackoverflow.com/questions/71409466/how-to-access-admin-firestore-using-firebase-admin-sdk)
- [storage](https://firebase.google.com/docs/storage/admin/start?hl=es-419)
- [translate_v2](https://cloud.google.com/translate/docs/reference/libraries/v2/python)
- [os](https://docs.python.org/es/3.10/library/os.html)
- [texttospeech](https://cloud.google.com/dotnet/docs/reference/Google.Cloud.TextToSpeech.V1/latest/Google.Cloud.TextToSpeech.V1.TextToSpeech.TextToSpeechClient?gad_source=1&gclid=CjwKCAjw-O6zBhASEiwAOHeGxZBTbt71obPANN32ZvSRi7k721C4Ogedqxap22FtLPSk349O-IZEyBoCQboQAvD_BwE&gclsrc=aw.ds)
- [io](https://docs.python.org/es/3.9/library/io.html)
- [pygame](https://www.pygame.org/docs/tut/ImportInit.html)
- [speech_recognition](https://pypi.org/project/SpeechRecognition/2.1.3/)
- [threading](https://docs.python.org/3/library/threading.html)
- [re](https://docs.python.org/3/library/re.html)
- [json](https://docs.python.org/3/library/json.html)
- [pyrebase](https://pypi.org/project/Pyrebase/)
- [requests](https://www.w3schools.com/python/module_requests.asp)
- [Nominatim](https://geopy.readthedocs.io/en/stable/)
- [EarthLocation](https://astropy-astrofrog.readthedocs.io/en/latest/coordinates/)
- [AltAz](https://astropy-astrofrog.readthedocs.io/en/latest/coordinates/)
- [get_sun](https://astropy-astrofrog.readthedocs.io/en/latest/coordinates/)
- [get_moon](https://astropy-astrofrog.readthedocs.io/en/latest/coordinates/)
- [get_constellation](https://astropy-astrofrog.readthedocs.io/en/latest/coordinates/)
- [SkyCoord](https://astropy-astrofrog.readthedocs.io/en/latest/coordinates/)
- [Time](https://docs.astropy.org/en/stable/time/)
- [units](https://docs.astropy.org/en/stable/units/)
- [numpy](https://numpy.org/doc/stable/user/absolute_beginners.html)
- [datetime](https://docs.python.org/es/3/library/datetime.html)
- [pytz](https://pypi.org/project/pytz/)
- [cv2](https://pypi.org/project/opencv-python/)
- [matplotlib.pyplot](https://matplotlib.org/2.0.2/users/pyplot_tutorial.html)
- [combinations](https://docs.python.org/3/library/itertools.html)
- [KDTree](https://docs.scipy.org/doc/scipy/reference/generated/scipy.spatial.KDTree.html)
- [tempfile](https://docs.python.org/3/library/tempfile.html)
- [socket](https://docs.python.org/3/library/socket.html)
- [Image](https://pillow.readthedocs.io/en/stable/reference/Image.html)
- [timedelta](https://docs.python.org/es/3/library/datetime.html)

Hardware:
- [Raspberry Pi 3b](https://www.raspberrypi.com/documentation/)
- [Raspberry Cam](https://github.com/OriolGarriga/STARGAZER/blob/main/Hardware/CAMV2.pdf)
- [x2 Stepper Motor 28BYJ-48](https://github.com/OriolGarriga/STARGAZER/blob/main/Hardware/Stepper%20Motor%20-%2028BYJ-48.PDF)
- [x2 Driver ULN2003](https://github.com/OriolGarriga/STARGAZER/blob/main/Hardware/Driver%20-%20ULN2003.PDF)
- Power Bank
- Laser

# Project Module
<p align="center">
  <img src="https://github.com/JoanEstopCepero/StarGazer/blob/main/img/diagrama_de_m%C3%B2duls.jpeg" width="500" />
</p>

# Hardware Architecture
<p align="center">
  <img src="https://github.com/JoanEstopCepero/StarGazer/blob/main/img/fritzing.png" width="500" />
</p>

# Algorithms
## Voice Communication

A voice communication feature was implemented using Google’s **Speech-to-Text** and **Text-to-Speech** APIs. This allows users to interact with the robot through spoken commands, enabling a hands-free and more natural user experience. The robot can interpret voice inputs and respond with synthesized speech, creating a more intuitive interface for controlling its functions.

## Constellation Detection from Sky Photographs

This feature enables the robot to identify and visualize constellations directly from user-provided images of the night sky, whether taken with the robot’s onboard camera or uploaded via the mobile app. To achieve this, we had to solve two main problems:

### 1. Identifying the Constellation in the Input Image

The first challenge was determining which constellation appears in the image. To do this, we implemented a **homography-based matching system**, which compares the input image to reference constellation images. The homography helps not only in identifying the most likely matching constellation, but also in estimating the **rotation angle**, **scaling factor**, and **alignment** needed to overlay the reference constellation onto the input image correctly.

Initially, our approach used **RANSAC** to detect key points and corners for feature matching. However, since the sky images mainly contain isolated star points (rather than textured features), RANSAC failed to find enough reference points for accurate homography estimation.

To overcome this, we enhanced both the reference images and the input image by **connecting the stars with their known constellation lines**, effectively transforming the visuals from sparse points into structured graphs. This approach significantly improved feature detection and allowed the homography to perform successfully.

### 2. Matching Stars to Draw the Constellation Overlay

Once the input image was aligned with the reference using homography, we applied a **KD-tree algorithm** to match the stars in the input image with those in the reference constellation. After establishing the correspondences, we used a predefined database of star connections (the line segments that define the shape of the constellation) to draw those lines **directly onto the original sky photo**.

As a result, the user can clearly see the constellation as it appears in their own sky photo, with the star connections visualized in place—bringing the abstract patterns of the stars into a concrete, personalized view.

<p align="center">
  <img src="https://github.com/JoanEstopCepero/StarGazer/blob/main/img/constellation%20detection.png" width="500" />
</p>

## From Location and Time to Stepper Motor Angles

Using the **user's input** (geographic coordinates, date, and time) along with the **Right Ascension (RA)** and **Declination (DEC)** of the selected star—retrieved from a Firestore database—we calculate the **azimuth** and **altitude** angles required to point the robot's laser accurately.

In this system:
- **Azimuth** corresponds to the **horizontal (X-axis)** direction,
- **Altitude** corresponds to the **vertical (Y-axis)** elevation.

With these two angles computed, the robot converts them into **stepper motor movements**, allowing it to physically aim at the celestial object requested by the user. This transformation from astronomical coordinates to motor control enables precise and automated star pointing.

# Images
<p align="center">
  <img src="https://github.com/JoanEstopCepero/StarGazer/blob/main/img/cupula%20img.jpeg" width="500" />
</p>

<p align="center">
  <img src="https://github.com/JoanEstopCepero/StarGazer/blob/main/img/robot%20%2B%20cupula.jpeg" width="500" />
</p>

<p align="center">
  <img src="https://github.com/JoanEstopCepero/StarGazer/blob/main/img/robot_i_c%C3%BApula.jpeg" width="500" />
</p>


# 3D
You can find a folder named [3D](https://github.com/JoanEstopCepero/StarGazer/tree/main/3D) with all the 3D modeling. Here is the main 3D model:
<p align="center">
  <img src="https://github.com/JoanEstopCepero/StarGazer/blob/main/img/3d%20model.gif" width="500" />
</p>

# Video
https://youtu.be/jfED0y5So1w

# References
https://www.hackster.io/starpointer/sshs-cs-7-3-starpointer-a60eb2

https://sketchfab.com/3d-models/laser-pointer-star-finder-robot-4288273bca724799888e1a2dc5643dc5

https://www.astropractica.org/oper/cnttel/cnttel.htm

http://www.jjrobots.com/

# Authors
Project developed by 
- Joan Estop Cepero
- Marçal Muñoz Salat
- Gerard Atienza Reig
- Oriol Garriga Puig
