# YoloOnColab
Use the following code to train any custom data set on YOLO. This can be even used by any beginner

Code for training: 
https://colab.research.google.com/drive/1s9vi9hyoKxQmEetZP58vwrRYXZBmC0ql 

Steps for training custom dataset:

1. Collect dataset from already present ones or download images from google. However please do note that the maximum the better. Please do have a minimum of 1000 images.
2. Annotate dataset in yolo format. There are some already existing apps like HyperLabel for windows or many github codes for linux(Bbox,AlexaayAB etc)
3. Create obj.data and obj.names file: obj.names would just have the names of classes of objects that are to be trained.
4. Create train.txt. It should have all the names of the images file present. Include " data/img/" before each file, as that would be the original data positions while training.
5. Zip all of them together. Ie train.txt,obj.data,obj.names and img. Img contains images and annotations. >>yolo-dataset.zip
6. Add a folder in your drive as ml. Upload the zip file in it.
7. Run the colab code. Make change in the part where the configuartion file is being updated. These values depend on the number of classes that you are going to train for.
8. Keep saving the weights to the drive every 100 epoch.

-example for obj.data:"

  classes= 5
  
  train  = data/train.txt
  
  valid  = data/train.txt
  
  names = data/obj.names
  
  backup = backup/
  
  
  
  "Change only the first line in this to change number of classes. 
  The class would be specified in annotation file, hence the train.txt file would contain the full images of all the classes.
Other links :

https://medium.com/@manivannan_data/how-to-train-yolov3-to-detect-custom-objects-ccbcafeb13d2  Check this link for more datails. 

https://www.tejashwi.io/training-yolov3-using-custom-dataset-on-google-colab/ : code from this link. 

https://timebutt.github.io/static/understanding-yolov2-training-output/

