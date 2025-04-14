# Camera Surveillance System
## Object Tracking and Identification using OpenCV and YOLO framework 

## Installation - READ FIRST! ##
### The necessary modules and packages are stored in the requirements.txt ###
Install the text file FIRST!! before running any of the scripts or else it won't work! 
- TYPE py -m pip install -r requirements.txt in your python environment terminal to execute text file
- For MAC USERS use python -m pip install -r requirements.txt

#### The Webcam Script  #######
- It will track any movement from the video footage
- Identify the object that is on screen and display a label
- The script attached will seek permission from camera and identify any object from the footage

#### Dashbaord Script ####
- The Dashboard is the user interface where I control can control the review and edit the slips stored
- Every script run is stored under the 'output_videos' folder, this GUI will list all the files in that folder
- The user can watch the clips, Rewind, Fastforward, and Delete clips at will
- Deleted clips are permanently deleted from the file system as well

#### Surveillance Script ####
- This script will play stored video clips from different scenarios and apply AI algorithm to identify objects
- The objects in the clips will be catergorised and tracked showcasing the capabilities of the OpenCV & YOLO framework
  
#### sentGmail script ###
- When a person is detected, it captures a screenshot
- Sends an email alert with the screenshot attached
- It helps to identify house pets i.e cats and dogs
- It works in low light conditiosn like at night

## Dataset
[UCF-Crime Dataset](https://webpages.charlotte.edu/cchen62/dataset.html)

## Architecture
#### Model Architecture
A video consists of an ordered sequence of frames. Each frame contains spatial information, and the sequence of those frames contains temporal information. To model both of these aspects, we use a hybrid architecture that consists of convolutions (for spatial processing) as well as recurrent layers (for temporal processing).

The first model i.e., CNN will be used to extract the (spatial) features and convert them into an encoded feature vector hence called an encoder. Similarly, the second model i.e., RNN will be used to process mini-batches of encoded frames to get the final classification result hence called a decoder.


#### Video Processing Pipeline
For real-time video monitoring, an efficient video streaming pipeline is required to handle the video stream from CCTV in parallel to the inference of models using those frames and make the best use of available hardware resources to minimize latency. Hence in video streaming engine, we used multiprocessing to create two different parallel processes, one of them handles the video streaming from CCTV or any other video input device and the other process will handle the inference engine for parallel analyzing the video frames for classification.



## Training

### [Output Images]
Here are the output screenshots from the app:

[*Video Playlist GUI*]
![Video_Playlist_GUI](https://github.com/RoninSanta/CM3070-Camera-Surveillance-System-Project/assets/109457795/3610c982-b157-491a-b991-e6dc27d6ae72)

[*Object Identification*]

![Object_Identification](https://github.com/RoninSanta/CM3070-Camera-Surveillance-System-Project/assets/109457795/488336cc-da2e-47f1-b519-0502f63fd09e)
-It has successfully identified the dog and the tennis ball in the moving footage

[*Intruder Alert*]
![Intruder Alert](https://github.com/RoninSanta/CM3070-Camera-Surveillance-System-Project/assets/109457795/dd9d1d18-86c8-4e26-9362-65ccf6644b38)
- When an intruder has been detected, the system sends out an alert and the camera will track the movements of the intruder

#### Size Issue ####
- The yolov3.weights is currently over 200MB therefore, you might have an issue trying to download it
- However, it is very crucial since it contains the pre-trained model for the classifier

                                                  Designed by © cybertech
