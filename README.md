# ANPR_IR
 Automatic Number Plate Recognition
 ##### Iranian Cars Number Plate


# STEP_1: Plate Detection with YOLOV7
## Run train_Yolov7.ipynb 
##### Dataset01: https://github.com/roozbehrajabi/ALPR_Dataset  /(YOLOv3_Dataset)
##### Dataset02: https://www.kaggle.com/datasets/skhalili/iraniancarnumberplate
##### Steps to download Kaggle datasets in Google Colab: https://www.kaggle.com/general/156610

## Result train_Yolov7.ipynb:
##### P = 0.985  --  R = 0.992  -- mAP@.5 = 0.995 -- mAP@.5:.95 = 0.779
                       
 
## Detect Plate: 
![01_plate_region](https://user-images.githubusercontent.com/51045212/219572532-8bb25396-2bc0-49f4-a108-d239badc31d2.jpg)

## Crop Plate Region:
![02_crop_region](https://user-images.githubusercontent.com/51045212/219572612-f3171679-7330-4165-903e-6d55b8d32150.png)


# STEP_2: OCR Plate Numbers with fasterrcnn_resnet50
##### Run tarin_ocr_fasterrcnn.ipynb

##### Dataset01: https://github.com/roozbehrajabi/ALPR_Dataset  /(Faster_R-CNN_dataset)
##### Install Detecto package for train fasterrcnn_resnet50:
##### https://detecto.readthedocs.io/en/latest/index.html
##### pip install detecto

## OCR Plate Numbers:
![03_ocr_plate_numbers](https://user-images.githubusercontent.com/51045212/219572807-4ee2db35-cdee-4223-ad8b-3ece2fbc0d9e.png)


# ANPR: ANPR/Yolov7_ANPR.py
##### Cloning Yolov7 repository in "/ANPR_IR/ANPR/" directory
##### Yolov7: https://github.com/WongKinYiu/yolov7
##### pip install deep-sort-realtime
##### pip install detecto
##### change font path in "/yolov7-main/utils/plots.py/def plot_one_box_PIL()" like "/ANPR_IR/ANPR/plots.py"
##### Run Yolov7_ANPR.py
### Test Image ANPR: get_plates_from_image(plate_image)
### Test Video ANPR: get_plates_from_video(video_path)
### Test Webcam ANPR: get_plates_from_webcam()

# ANPR:
![04_detected_plate](https://user-images.githubusercontent.com/51045212/219576614-1fe1bd35-4ecf-48da-a16f-f7e570df75da.png)
