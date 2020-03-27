# [Door Detection & Classification] Dataset
This dataset was built for door object detection, classification and semantic segmentation. \
The images were obtained using a 3D Realsense Camera, model D435. The camera was rotated 90 degrees since its horizontal viewing angle(86 degrees) is bigger than its vertical viewing angle(57 degrees) with the purpose of including all the door area in the images.
The images captured are from Universidade da Beira Interior, public places and people's houses with several doors and its surroundings with different textures and sizes. \
The [Door Detection & Classification] Dataset is divided in two sub-datasets, one for door detection/semantic segmentation with 240 images and the other for door classification with 1206 images. \
Further details of the sub-datasets are described below.


## Door Detection | SemanticSegmentation SubDataset
This subdataset has a total of 240 grey-scaled images with the size 480 x 640. The pixel value of the images is 1 if it corresponds to a door or door frame, and is 2 if it does not.

[image]

## Door Classification SubDataset [3D and RGB]
This subdataset has a total of 1206 rgb door images and the 1206 corresponded depth images.
Both with the size 480 x 640 pixels. The depth images are in grey-scale with pixels values between 0 and 255 and the depth scale used was equal to 1/16. The depth in meters is equal to depth scale * pixel value, for example, if the pixel value is equal to 32 it means that that pixel is 2 meters away from the viewer(1/16 * 32 = 2). 
The dataset has 468 closed door images, 588 open door images and 150 semi-open doors images. It is also divided in test, validation and train set. For the validation and test set it were used 20 samples of each class giving a total of 60 samples for test and 60 samples for validation. The remaning samples were used to built the training set (1086 images).
This subdataset is divided in two parts, "Original Size" and "Cropped". The original size has the images with the original size (480 x 640) and the cropped divisions has the same images but cropped acording to the location of the door and door frame. 

## Link to dataset
Link [here](https://drive.google.com/drive/folders/1iSrPjO-F2aaB7MmsN7tsU1wnLtnO3euK?usp=sharing)


## Data Structure
Door Detection & Classification Dataset
* Door Detection
  * Annotations
    * Test
    * Train
  * Images
    * Test
    * Train
  
* Door Classification
  * Cropped (Just the door and doorframe in the image)
    * Depth
      * Test
        * Closed
        * Open
        * Semi-open
      * Train
        * Closed
        * Open
        * Semi-open
      * Val
        * Closed
        * Open
        * Semi-open
    * RGB
      * Test
        * Closed
        * Open
        * Semi-open
      * Train
        * Closed
        * Open
        * Semi-open
      * Val
        * Closed
        * Open
        * Semi-open   
  * OriginalSize (original size image - 480 * 640)
    * Depth
      * Test
        * Closed
        * Open
        * Semi-open
      * Train
        * Closed
        * Open
        * Semi-open
      * Val
        * Closed
        * Open
        * Semi-open
    * RGB
      * Test
        * Closed
        * Open
        * Semi-open
      * Train
        * Closed
        * Open
        * Semi-open
      * Val
        * Closed
        * Open
        * Semi-open   
       
 ## Citation
 If you use this dataset, please cite:
```
 @InProceedings{icarsc2020,
  author = {João Gaspar Ramôa and Luís A. Alexandre and Sandra Mogo},
  title = {Real-Time 3D Door Detection and Classification on a Low-Power Device},
  booktitle = {20th IEEE International Conference on Autonomous Robot
Systems and Competitions (ICARSC 2020)},
  year = {2020},
  address = {Azores, Portugal},
  month = {April}
}
```
