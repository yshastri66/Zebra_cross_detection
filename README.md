# Zebra_cross_detection
This is My project which detects Zebra cross along the road from driver's point of view. Its more useful on autonomous cars.
Here I used 1024*1024 pixel images which almost covers all real life camera images.For training purpose I used 
[nuScenes](https://www.nuscenes.org/) dataset which consists of 67k images.Out of which I selected <b>2.5k</b> images with zebra cross for training purpose. I had also included 
some custom images from my camera.So,it works well with high resolution images.I had trained the model on <b>Tensorflow 2 Object Detection</b> which is the latest
tensorflow object detection module.I used <b>SSD_Resnet50_1024x1024 </b> model for training.It gave <b>DetectionBoxes_Precision/mAP@.50IOU : 82% .</b>
Its good since we have a lot of corner cases in the dataset like faded zebra cross,half cut zebra cross due to vehicles,angle with which zebra cross is visible to car.
We can detect zebra cross with high accuracy if we include 3D detection.For cases in 2D,This model performs better.<br><br>
<img src="https://github.com/yshastri66/Zebra_cross_detection/blob/master/sample_predictions/test-1770.jpg" width="700" height="500">
<br><br>Its also detecting even if the zebra cross is not fully visible : <br>
<img src="https://github.com/yshastri66/Zebra_cross_detection/blob/master/sample_predictions/train-2801.jpg" width="700" height="500">

## Steps for testing the model with images :
### 1.Clone this repository by downloading zip or by running following command in Git or terminal :
```
git clone https://github.com/yshastri66/Zebra_cross_detection.git
```

### 2.Create a new python environment and install the requirments using requirment.txt file by executing following commands :
```
conda create -n env_name
conda activate env_name
pip install -r requirments.txt
```
### 3.Put all your images which you want to detect in <b>'test'</b> folder.
### 4.Run the jupyter notebook image_testing.ipynb
### 5. comment out following lines if you are not using GPU :
```
physical_devices = tf.config.list_physical_devices('GPU')
tf.config.experimental.set_memory_growth(physical_devices[0],True)
```
### 6. All your images with predictions will be saved in predictions folder.
Sample predicted images are given in the folder <b>sample_predictions</b>. Look into it for better understanding.
#### Feel free to contact me if you are having any douts.
#### contact : yashodharashastri6@gmail.com
