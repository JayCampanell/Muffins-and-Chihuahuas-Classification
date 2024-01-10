# Muffins-and-Chihuahuas-Classification
CAIS++ Winter Curriculum Project

## Jay Campanell 	 jcampane@usc.edu

I present Muffins or Chihuahua, to distinguish between the two I built upon the EfficientNetB3 Model.


## Dataset: 
I chose to use the Muffins or Chihuahua dataset. The only preprocessing I performed on the data was reducing all images down to 170x170. I chose to do this to try and decrease the amount of time it takes to train the model.

## Model Development and Training: 
I decided to use the EfficientNetB3 model to build upon my model. I chose it because it could outperform ResNet, which is what I originally chose based on a quick search, both in terms of computational power and accuracy. I also settled on B3 because I felt it had a good compromise between the amount of computational power it needed for the accuracy it was getting. I also chose Adam and a learning rate of .0001 because after testing different optimizers and learning rates I got the best results from this specific combination. 

## Model Evaluation/Results:
After 11 epochs the model had an accuracy of .9467 and using the test data the accuracy was .9527



## Discussion: 
For the architecture, I turned off base layers from EffecientNetB3 and made them untrainable so the training process would be faster. In addition to the pre-trained layers, I added a few on top so the model could be better trained for classifying muffins and chihuahuas. In the beginning, I was using a different pooling method and was getting overfitting so I added the dropout layer to reduce the overfitting. I decided to use a global average pooling because it could retain more information than max pooling. I thought the distinctions between the images were more nuanced, so retaining as much information as possible was important. I think being able to classify images is highly beneficial and although this specific model was built on the trivial task of being able to classify dogs from muffins the same methods and ideas can be applied to projects which more social impact. I would be wary though because the dataset that I used was pretty clean, with already clear and labeled data, the images also only contained one subject and were classified on that one subject. So if wanting to retrain the model on a more complex problem with multiple subjects and less tidy data the model may not perform as well. In the future I would want to pull new images that were not used in the dataset to see if the model could still perform as well as maybe connecting it to a video stream and seeing if it could make its distinctions in real time. 
