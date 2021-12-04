# Object-Detection (YOLOv4)

1. **Bounding Box** (Creating Labels/Annotations)- 
* The Json file of annotation does not contain the bounding box coordinate
* Created manually the bounding box on image dataset using **LabelImg** Tool https://github.com/tzutalin/labelImg -- tooks to much time to build bounding box around each image. 

![labelimgtool](https://user-images.githubusercontent.com/39665134/144701896-478530d6-54b6-4868-91c9-7654cef84057.PNG)

2. **Downloaded annotated images** from huge dataset.
* Downloaded anotated and labelled dataset (containing bounding box values) from google open images dataset with Person & Car class.
* Category = [Person, Car]
* Clone the repo - https://github.com/EscVM/OIDv4_ToolKit to download dataset (Dataset) and annotation (csv_folder) from open image dataset.

![Download Image](https://user-images.githubusercontent.com/39665134/144703163-3583cff6-ea89-439e-a963-c2ddb150e62d.PNG)


3. Converting images in yolo format
* Generate file that contain class and bounding box info along with image dataset. 
* Format - 
main_folder
│   main.py
│
└───OID
    │   file011.txt
    │   file012.txt
    │
    └───csv_folder
    |    │   class-descriptions-boxable.csv
    |    │   validation-annotations-bbox.csv
    |
    └───Dataset
        |
        └─── test
        |
        └─── train
        |
        └─── validation
             |
             └───Apple
             |     |
             |     |0fdea8a716155a8e.jpg
             |     |2fe4f21e409f0a56.jpg
             |     |...
             |     └───Labels
             |            |
             |            |0fdea8a716155a8e.txt
             |            |2fe4f21e409f0a56.txt
             |            |...
             |
             └───Orange
                   |
                   |0b6f22bf3b586889.jpg
                   |0baea327f06f8afb.jpg
                   |...
                   └───Labels
                          |
                          |0b6f22bf3b586889.txt
                          |0baea327f06f8afb.txt
                          |...


* 

4. Make Data ready for training purposes 

4. Training on COCO Dataset (80 Classes)

5. Training on Custom Dataset (with only Person-Car Class)
