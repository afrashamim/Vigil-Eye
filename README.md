# 👁️ Vigil Eye: Driver Drowsiness Detection System

Vigil Eye is a real-time driver monitoring system designed to detect drowsiness and alert the driver with an audible warning. Using computer vision, machine learning, and an intuitive graphical interface, this system provides a reliable solution to enhance road safety.

---

## ✨ Features

- 🔍 **Real-Time Eye Tracking**: Monitors the driver's eye movements using a webcam.
- 📊 **Eye Aspect Ratio (EAR)**: Calculates EAR to detect if the driver is drowsy.
- 🚨 **Audible Alert System**: Plays a sound alert when drowsiness is detected.
- 🖼️ **Graphical Interface**: User-friendly GUI for starting and stopping detection.
- 🧠 **Face Landmark Detection**: Leverages Dlib's pre-trained facial landmark predictor.

---

## 🛠️ How It Works

1. **Eye Aspect Ratio (EAR) Calculation**  
   - The program calculates EAR for both eyes using facial landmarks.  
   - A threshold (`0.25`) and frame-check count (`20`) are used to detect drowsiness.  

2. **Drowsiness Detection**  
   - If EAR falls below the threshold for 20 consecutive frames, an alert is triggered.

3. **Audio Alert**  
   - A warning sound (`music.wav`) is played to notify the driver.

4. **Graphical Interface**  
   - Users can start and stop the detection process with buttons in the GUI.

---


## ⚙️ Prerequisites

Before running the application, make sure you have:

- **Python 3.x** (recommended version: 3.7+)
- **OpenCV** for real-time video capture and processing.
- **dlib** for facial landmark detection.
- **imutils** for image resizing and handling.
- **pygame** for playing alert sounds.
- **scipy** for calculating distances and Eye Aspect Ratio (EAR).
- **Pillow** for image handling (used for GUI with Tkinter).



```bash
pip install scipy imutils pygame dlib opencv-python pillow
```


## 📋 Usage

 **Prepare the Required Files**
   - **Facial Landmark Model**: Download the [model](models/shape_predictor_68_face_landmarks.dat).
   - **Audio Alert**: Ensure (music.wav) is placed in the working directory.
   - **Background Image**: Update the path for `Interface.png` in the script.

     

## 🖼️ Graphical Interface

- **Background**: Displays a custom background image.
- **Buttons**:
  - **START DETECTION**: Initiates the drowsiness monitoring process.
  - **STOP DETECTION**: Stops the detection and closes the application.
 


## ⚠️ Notes

- Make sure your webcam is working and accessible by the program.
- Adjust the EAR threshold (`thresh`) and frame-check count (`frame_check`) for optimal performance.

  

  

## 📂 File Structure

```plaintext
.
├── vigilance_eye.py          # Main script
├── music.wav                 # Audio alert file
├── models/
│   └── shape_predictor_68_face_landmarks.dat # model file
└── Interface.png             # GUI background image


```



## 🔧 Further Enhancements

Here are a few ideas to enhance the functionality and performance of the drowsiness detection system:

1. **Multiple Alert Types**:
   - Add visual alerts such as flashing or color changes in the GUI when drowsiness is detected, alongside the audio alert.
   
2. **Real-Time Monitoring Statistics**:
   - Display real-time data such as the average Eye Aspect Ratio (EAR) or the number of consecutive frames where drowsiness was detected to provide additional insights.

3. **Customization of Alert Methods**:
   - Allow users to choose between different alert types (sound, vibration, notifications) for better user experience in varying environments.

4. **Mobile Compatibility**:
   - Adapt the system for mobile devices, using the device's front camera for drowsiness monitoring in mobile applications.

5. **Real-Time Feedback and Recommendations**:
   - Provide suggestions such as "Take a break" or "Drink some water" when drowsiness is detected, based on the detected severity of the condition.




