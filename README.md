# Python_YOLOV3

## linux_v1.4.0
The tools of label image.<br>
Or you can download here: <a> https://tzutalin.github.io/labelImg/


## Install OpenCV
>>      pip install opencv-python

## How to put data  
>>      Data--
>>        ↳ Images(.jpg,.png ...)
>>        ↳ Labels(.xml)
>>        ↳ Yolos(Inside data will make by code)
>>        ↳ Test_image
>>        ↳ Test_xml
>>        ↳ Test_image_yolo
## change_yolo_cfg.txt
>   ### Open ../cfg/yolov3.cfg <br>
>>      Line 6: set batch=24, this means we will be using 24 images for every training step
>>      Line 7: set subdivisions=8, the batch will be divided by 8 to decrease GPU VRAM requirements.
>>      Line 603: set filters=(classes + 5)*3 in our case filters=21
>>      Line 610: set classes=2, the number of categories we want to detect
>>      Line 689: set filters=(classes + 5)*3 in our case filters=21
>>      Line 696: set classes=2, the number of categories we want to detect
>>      Line 776: set filters=(classes + 5)*3 in our case filters=21
>>      Line 783: set classes=2, the number of categories we want to detect
   
## Train.py
>  ### Chage to your data path 
>>      xmlFolder = "/data/home/Labels" 
>>      imgFolder = "/data/home/Images" 
>>      saveYoloPath = "/data/home/Yolos"
>  ### Chage to your class    
>>      classList = { "stas":0 , "dog":1 }
>  ### Give the path, where you want to make a cfg.XXX floder
>>      cfgFolder = "/data/home/cfg.stas_yeh"

## tt_YOLO_iou.py

>  This one python code not only print the Bounding-Box but also print the original Bounding-Box and count the iou for you<br>

>  ### Chage to your data path

>>      classesFile = "/data/home/cfg.stas_yeh/obj.names";             
>>      modelConfiguration = "/data/home/cfg.stas_yeh/yolov3.cfg";   
>>      modelWeights = "/data/home/cfg.stas_yeh/weights/yolov3_10000.weights";

>>      path_out = '/data/home/Test_image_yolo/' ##output image file 
>>      path_in = '/data/home/Test_image/'       ##resd test image   
>>      path_xml = '/data/home/Test_xml/'        ##read test xml

## tt_all_YOLO.py

>  This one python code only print the Bounding-Box for you<br>
>  ### Chage to your data path

>>      classesFile = "/data/home/obj.names";             
>>      modelConfiguration = "/data/home/yolov3.cfg";   
>>      modelWeights = "/data/home/cfg.stas_yeh/yolov3_10000.weights";

>>      path_out = '/data/home/Test_image_yolo/' ##output image file 
>>      path_in = '/data/home/Test_image/'       ##resd test image   
   
