# YOLO v3 : Real Time Object Detection

You only look once (YOLO) is a state-of-the-art, real-time object detection system. On a Pascal Titan X it processes images at 30 FPS and has a mAP of 57.9% on COCO test-dev
YOLO is a system for detecting objects on the Pascal VOC 2012 dataset. It can detect about 20 Pascal object classes.

# But How?
The prior detection systems repurpose classifiers or localizers to perform detection. They apply the model to an image at multiple locations and scales. High scoring regions of the image are considered detections.
Here we use a totally different approach. We apply a single neural network to the full image. This network divides the image into regions and predicts bounding boxes and probabilities for each region. These bounding boxes are weighted by the predicted probabilities.

Wanna know more?        
https://bit.ly/2Cnv869

# Requirements
Anaconda – Python 3.7 (Windows 10) https://www.anaconda.com/download/


Conda Env yolov3.yml
https://github.com/astra-sv/yolov3/blob/master/yolov3.yml
   
     cd C:\yolo
     conda env create -f yolo.yml

If any errors popup, try installing from requirements.txt
   
    pip install -r requirements.txt
    
CUDA Toolkit - V9.0 (Nvidia GPU GTX 1050 or higher) https://bit.ly/2PRLjke

Ensure that you have the latest nvidia graphics drivers install on your PC.

# PyTorch 

Change directory to a workplace where you want to download.
Clone Yolo v3 Repo
    
     cd C:\yolotorch
Download test video (.mp4/.avi) 
Rename video to video_demo.mp4
     
      python video_demo.py --video video.mp4
To run demo on webcam
      
      python cam_demo.py


# Optional
If you get this error while running the webcam

       File "cam_demo.py" , line 123, in <module>
       im_dim=im_dim.cuda
       NameError: name 'im_dim' is not defined
       
Try opening cam_demo.py and uncomment the line 119

