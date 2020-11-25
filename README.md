# Zebra Crossing Detection
[![TensorFlow 2.2](https://img.shields.io/badge/TensorFlow-2.2-FF6F00?logo=tensorflow)](https://github.com/tensorflow/tensorflow/releases/tag/v2.2.0)
[![Python 3.6](https://img.shields.io/badge/Python-3.6-3776AB)](https://www.python.org/downloads/release/python-360/)<br>
### This is the model to predict the Zebra Cross in real time from driver's view.
![sample gif](https://github.com/iNeuron-ai/zebra_crossing/blob/main/demo/Hnet-image.gif)

### Key features are :

<ul>
  <li> This model is trained with 1024*1024 images which is of real time camera quality.</li>
  <li> I used [nuScenes](https://www.nuscenes.org/) deep drive dataset and also some custom images for training</li>
  <li> I took 2300 images out of 67k images from Nuscenes dataset and 200 real images from camera</li>
  <li> Here I used <b> Tensorflow 2 object detection</b> which is the latest object detection library of google </li>
  <li> I used SSD Resnet 50 1024*1024 model for training purpose </li>
  <li> I got <b> DetectionBoxes_Precision/mAP@.50IOU </b> nearly 82% which is good for 2D image detection in road.</li>
</ul>

### Steps to test the model:
#### 1.Clone this repository by downloading zip or by running following command in Git or terminal :
```
git clone https://github.com/yshastri66/Zebra_cross_detection.git
```

#### 2.Create a new python environment and install the requirments using requirment.txt file by executing following commands :
```
conda create -n env_name
conda activate env_name
pip install -r requirments.txt
```
#### 3.Put all your images which you want to detect in <b>'test'</b> folder.
#### 4.Run the jupyter notebook image_testing.ipynb
#### 5. comment out following lines if you are not using GPU :
```
physical_devices = tf.config.list_physical_devices('GPU')
tf.config.experimental.set_memory_growth(physical_devices[0],True)
```
#### 6. All your images with predictions will be saved in predictions folder.
Sample predicted images are given in the folder <b>sample_predictions</b>. Look into it for better understanding.

If you are having any douts, feel free to contact me.
### Contributor:
#### Yashodhara Shastri G
#### Contact : yashodharashastri6@gmail.com
