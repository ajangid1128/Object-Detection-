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


3. **Converting images in yolo format**
* Generate file that contain class and bounding box info along with image dataset. 
* Obtained CenterX, CenterY, width, height of bounding box and store in txt file.
* Format for yolo = Each Image + Each Annotation [classnumber,CenterX, CenterY, width, height]  

4. **Training on COCO Dataset (80 Classes)**
* Clone the repo: https://github.com/alexeyab/darknet
* Download weights trained on Coco Dataset pre-trained transfer learning

![weight](https://user-images.githubusercontent.com/39665134/144703626-2a5c0853-fc17-45a8-8b35-d9564a56242b.PNG)


* Used Google Colab GPU hardware system
* Compile our darknet model - open source neural network model. 

![DARKNET MODEL](https://user-images.githubusercontent.com/39665134/144703634-1eb99418-b470-44a8-bb17-0ca8a9b74fda.PNG)

![COCO](https://user-images.githubusercontent.com/39665134/144704198-a291eaec-191e-4da2-a00f-ca4558f15c20.PNG)


5. Training on Custom Dataset (with only Person-Car Class)
* Update yolov4 hyperparameters including classes = 2, filter = 21, max_batch_size = 4000 and generate two train_yolov4.txt & test_yolov4.txt file containing hyperparameters.  
*  Learn weights for our custom dataset.  

![customdataset](https://user-images.githubusercontent.com/39665134/144703939-de2ea59b-fad8-47df-8e77-19062ae4bb80.PNG)

![PersonCar](https://user-images.githubusercontent.com/39665134/144703740-5826158c-03c2-40fe-bf4c-544529add78c.PNG)
  



