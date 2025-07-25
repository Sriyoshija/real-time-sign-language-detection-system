# REAL-TIME SIGN LANGUAGE RECOGNITION SYSTEM                                                                                                                                                                        


## Project Overview                                                                                                                                                                                                       
A computer vision system that translates American Sign Language (ASL) alphabets (A-Y) to text in real-time using:                                                                                                       
-> MediaPipe for 21-point hand landmark detection (24 FPS)                                                                                                                                                                 
-> Custom CNN model (96.7% accuracy) trained on 7,000+ annotated images                                                                                                                                                         
-> OpenCV pipeline processing 640×480 video at 30 FPS                                                                                                                                                                    

<img width="134" height="679" alt="image" src="https://github.com/user-attachments/assets/4a73dabb-a1e0-417d-98e0-07fa022b44b0" />

## Key Features                                                                                                                                                                                                         
Real-time letter detection with 300ms latency                                                                                                                                                                                   
Word formation using space-delimited boundaries                                                                                                                                                                       

Interactive UI controls:                                                                                                                                                                                                                   
S Add letter                                                                                                                                                                                                          
X Backspace                                                                                                                                                                                                            
C Clear text                                                                                                                                                                                                          
PyInstaller-packaged executable for Windows/Linux                                                                                                                                                                     

## Installation                                                                                                                                                                                                         
Prerequisites :                                                                                                                                                          
Python 3.8+ (Pycharm)                                                                                                                                                                   
Webcam (minimum 720p resolution)     

## Required Libraries
opencv-python==4.7.0                                                                                                                                                    
mediapipe==0.10.11                                                                                                                                                         
tensorflow==2.9.1                                                                                                                                                     
cvzone==1.5.6                                                                                                                                                         
numpy==1.24.4

## Dataset Requirements
Add training images with:

Resolution: 300×300 pixels                         
Background: Solid white (RGB 255,255,255)                                       
Hand Position: Centered, palm facing camera

Variations:                                                 
Multiple skin tones                              
Different lighting conditions                                  
5°-15° rotation variations                                   
Slightly bent fingers                                    

Optimal Gesturing:                         
Position hand 30-50cm from webcam                               
Ensure even lighting (avoid backlight)                              
Hold gesture steady for 1-2 seconds  

## Process
1. Environment Configuration

Established Python 3.8 virtual environment in PyCharm with OpenCV , TensorFlow , and cvzone libraries, validated with 30 FPS webcam feed using cv2.VideoCapture(0).

2. Dataset Creation

Collected 7,500 hand-cropped ASL images (300×300px RGB) across 25 letters (A-Y), maintaining white background consistency through automated padding and aspect ratio preservation.

3. CNN Model Development

Trained Teachable Machine model for 50 epochs (batch=32) achieving 96.7% validation accuracy, exported as TensorFlow (keras_model.h5) and TFLite formats for production deployment.

4. Real-Time Recognition System

Implemented hand detection pipeline using cvzone.HandDetector with letter sequencing UI (S/X/C keys) and error correction logic, achieving 24ms inference time through model quantization.

## Features   
The features that we have in this project are:                                              
- Python 3.8 environment with OpenCV and TensorFlow configured in PyCharm IDE, validated through 30 FPS webcam feed testing.                        
- 7,500 standardized ASL images (300×300px RGB) collected across 25 letters using automated cropping/padding techniques.                       
- CNN model trained via Teachable Machine (50 epochs) achieving 96.7% validation accuracy, exported as TensorFlow/TFLite formats.                      
- Real-time recognition system operating at 24ms inference speed with hand tracking and text editing controls (S/X/C keys).                       
- Deployable 148MB executable containing compressed model files and operational guidelines for end-users.                                              

## Contact

*Email:* [GMAIL](sriyoshijachokka@gmail.com)                                               
*LinkedIn:* [CHOKKA SRIYOSHIJA](www.linkedin.com/in/chokka-sriyoshija-77a82b295)                       
