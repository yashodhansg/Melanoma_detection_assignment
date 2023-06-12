# Multiclass classification model development using a custom convolutional neural network in TensorFlow to accurately detect Melanoma.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)


## General Information
- # Background of the project :   
- Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis. 
- # Problem being solved :  
- The purpose of the project is to develop a CNN based model which can accurately classify the input images into appropriate skin cancer type. Model is trained to classify total 9 types of skin cancer. The special interest is to be able to detect Melanoma which is one of the deadliest cancer type. 
- # Dataset being used :  
- The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC. Data belongs to total 9 classes each representing a type of cancer. 



## Conclusions
- # Models built :
- Total 4 models were built to solve the problem. Each model consists of 15 weight layers. However, 1st model did not have any drop-out layer, normalization layer, augmentation strategy. Also, it was trained on original data which had significant class imbalance. For 2nd model,augmentation strategy of randomflip and random rotation were used. It was also trained on original data which had significant class imbalance. 3rd model had batch normalization incoporated. Also, class imbalance was removed by adding 500 images of each class using augmentor package.MOdel4 is same as model3 but also has drop-out layer added.   
- # Comparison of Models :
- 1st and 2nd model had very low training as well as validation accuracy indicating underfitting. However, 3rd model gave satisfactory performance with training accuracy of more than 90%. Also, for 3rd model validation accuracy closely followed training accuracy indicating not much overfitting.4rth model did not seem to over any significant improvement over 3rd model.1st model and 2nd model are clearly not acceptable. 4rth model seems ok. However, 3rd model seems to be the best model.   
- # Possible reason for difference in performance of model :  
- The third model was trained on data where classes were balanced by adding 500 images to each class by using augmentor package. Also, batch normalization was used. Either of the two or both of these factors seem to have contributed to significant improvement in model performance compared to 1st and 2nd model. 4rth model made use of drop-out layer which does not seem to be giving any significant advantage in our case based upon model results.  


## Technologies Used
- Augmentor version 0.2.12
- keras     version 2.12.0
- pathlib   version 1.0.1
- tensorflow version 2.12.0


<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
- We thank Upgrad for introducing the problem statement to us as a part of an assignment. 



## Contact
Created by Yashodhan[@yashodhansg], Shailesh, Vidhyasaghar - feel free to contact us!



