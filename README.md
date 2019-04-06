# Python_YOLOV3

## linux_v1.4.0
The tools of label image.<br>
Or you can download here: <a>https://tzutalin.github.io/labelImg/

## How to put data 
   xmlFolder
   imgFolder
   saveYoloPath
## change_yolo_cfg.txt
>   ### Open ../cfg/yolov3.cfg <br>
   Line 6: set batch=24, this means we will be using 24 images for every training step<br>
   Line 7: set subdivisions=8, the batch will be divided by 8 to decrease GPU VRAM requirements.<br>
   Line 603: set filters=(classes + 5)*3 in our case filters=21<br>
   Line 610: set classes=2, the number of categories we want to detect<br>
   Line 689: set filters=(classes + 5)*3 in our case filters=21<br>
   Line 696: set classes=2, the number of categories we want to detect<br>
   Line 776: set filters=(classes + 5)*3 in our case filters=21<br>
   Line 783: set classes=2, the number of categories we want to detect<br>
   
## Train.py
>  ### chage to your data path 
   xmlFolder = "/data/home/Labels" <br>
   imgFolder = "/data/home/Images" <br>
   saveYoloPath = "/data/home/Yolos" <br>
>  ### chage to your class    
   classList = { "stas":0 , "dog":1 } <br>
>  ### give the path, where you want to make a cfg.XXX floder
   cfgFolder = "/data/home/cfg.stas_yeh" <br>
