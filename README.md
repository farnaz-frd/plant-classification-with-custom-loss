# plant-classification-with-custom-loss
This project is about classifying plant images with an additional Boolean tag that indicates the truth of the label. For example, if the label is “sansevieria” and the tag is false, it means that the related image is not “sansevieria”.
A custom loss function is used to help the model take into account the tags during training. If the tag is false and the model predicts any other label than what has been written in the related column label, it’s okay and the loss must not increase.

The dataset used for creating the model consists of about 66000 images and can be found here: 
https://drive.google.com/file/d/1G7eDJEfuuYzh62rZ26JlvSRaK-VvyKjm/view?usp=share_link. 
The labels and tags for the images are stored in ordibehesht.csv. 
The labels are not ordered by images and must be searched by the image’s address. The code for this is included in the project.

The custom loss has been calculated based on the below table:

![truth_table](https://user-images.githubusercontent.com/53252795/235314769-8f3c9342-f054-4c69-aaf2-9ee14ba12186.png)
