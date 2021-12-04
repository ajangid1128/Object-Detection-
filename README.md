# Object-Detection (YOLOv4)

1. **Bounding Box** (Creating Labels/Annotations)- 
* The Json file of annotation does not contain the bounding box coordinate
* Created manually the bounding box on image dataset using **LabelImg** Tool https://github.com/tzutalin/labelImg -- tooks to much time to build bounding box around each image. 

![labelimgtool](https://user-images.githubusercontent.com/39665134/144701896-478530d6-54b6-4868-91c9-7654cef84057.PNG)

2. **Downloaded annotated images** from huge dataset.
* Downloaded anotated and labelled dataset (containing bounding box values) from google open images dataset with Person & Car class. 

3. Converting images in yolo format

4. Make Data ready for training purposes 

4. Training on COCO Dataset (80 Classes)

5. Training on Custom Dataset (with only Person-Car Class)
