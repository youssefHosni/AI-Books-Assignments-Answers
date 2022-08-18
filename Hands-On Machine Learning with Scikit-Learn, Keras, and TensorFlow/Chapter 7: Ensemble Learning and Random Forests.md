# Chapter 7: Ensemble Learning and Random Forests #

## Questions ##

[1. If you have trained five different models on the exact same training data, and they all achieve 95% precision, is there any chance that you can combine these models to get better results? If so, how? If not, why?](https://github.com/youssefHosni/AI-Books-Assignments-Answers/blob/main/Hands-On%20Machine%20Learning%20with%20Scikit-Learn,%20Keras,%20and%20TensorFlow/Chapter%207:%20Ensemble%20Learning%20and%20Random%20Forests.md#:~:text=1.%20If%20you%20have%20trained%20five%20different%20models%20on%20the%20exact%20same%20training%20data%2C%20and%20they%20all%20achieve%2095%25%20precision%2C%20is%20there%20any%20chance%20that%20you%20can%20combine%20these%20models%20to%20get%20better%20results%3F%20If%20so%2C%20how%3F%20If%20not%2C%20why%3F)

[2. What is the difference between hard and soft voting classifiers?](https://github.com/youssefHosni/AI-Books-Assignments-Answers/blob/main/Hands-On%20Machine%20Learning%20with%20Scikit-Learn,%20Keras,%20and%20TensorFlow/Chapter%207:%20Ensemble%20Learning%20and%20Random%20Forests.md#:~:text=2.%20What%20is%20the%20difference%20between%20hard%20and%20soft%20voting%20classifiers%3F)

3. Is it possible to speed up training of a bagging ensemble by distributing it across multiple servers? What about pasting ensembles, boosting ensembles, random
forests, or stacking ensembles?

4. What is the benefit of out-of-bag evaluation?

5. What makes Extra-Trees more random than regular Random Forests? How can this extra randomness help? Are Extra-Trees slower or faster than regular Random Forests?

6. If your AdaBoost ensemble underfits the training data, what hyperparameters should you tweak and how?

7. If your Gradient Boosting ensemble overfits the training set, should you increase or decrease the learning rate?

8. Load the MNIST data (introduced in Chapter 3), and split it into a training set, a validation set, and a test set (e.g., use 50,000 instances for training, 10,000 for validation, and 10,000 for testing). Then train various classifiers, such as a Random Forest classifier, an Extra-Trees classifier, and an SVM. Next, try to combine them into an ensemble that outperforms them all on the validation set, using a soft or hard voting classifier. Once you have found one, try it on the test set. How much better does it perform compared to the individual classifiers?

9. Run the individual classifiers from the previous exercise to make predictions on the validation set, and create a new training set with the resulting predictions: each training instance is a vector containing the set of predictions from all your classifiers for an image, and the target is the image’s class. Train a classifier on
this new training set. Congratulations, you have just trained a blender, and together with the classifiers they form a stacking ensemble! Now let’s evaluate the ensemble on the test set. For each image in the test set, make predictions with all your classifiers, then feed the predictions to the blender to get the ensemble’s predictions. How does it compare to the voting classifier you trained earlier?

----------------------------------------------------------------------------------------------------------------------------------------------------------------


## Questions & Answers ##

**1. If you have trained five different models on the exact same training data, and they all achieve 95% precision, is there any chance that you can combine these models to get better results? If so, how? If not, why?**

Answer:

Yes, using ensamble method, in which you will train each model on the training data and use hard or soft (if possible depedning on the model used) voting to get the prediction. You can also train them using different subset of the data using bagging or pasting method.  

**2. What is the difference between hard and soft voting classifiers?**

Answer:

In hard voting the class that get most of the votes will be selected, while in soft voting the probability for each class is averaged throughout all the classifers in the ensemble learners and the class with the heighest probability will be selected. 


**3. Is it possible to speed up training of a bagging ensemble by distributing it across multiple servers? What about pasting ensembles, boosting ensembles, random
forests, or stacking ensembles?**

Answer:


**4. What is the benefit of out-of-bag evaluation?**

Answer:


**5. What makes Extra-Trees more random than regular Random Forests? How can this extra randomness help? Are Extra-Trees slower or faster than regular Random Forests?**
Answer:


**6. If your AdaBoost ensemble underfits the training data, what hyperparameters should you tweak and how?**

Answer:



**7. If your Gradient Boosting ensemble overfits the training set, should you increase or decrease the learning rate?**

Answer:


**8. Load the MNIST data (introduced in Chapter 3), and split it into a training set, a validation set, and a test set (e.g., use 50,000 instances for training, 10,000 for validation, and 10,000 for testing). Then train various classifiers, such as a Random Forest classifier, an Extra-Trees classifier, and an SVM. Next, try to combine them into an ensemble that outperforms them all on the validation set, using a soft or hard voting classifier. Once you have found one, try it on the test set. How much better does it perform compared to the individual classifier?**

Answer:


**9. Run the individual classifiers from the previous exercise to make predictions on the validation set, and create a new training set with the resulting predictions: each training instance is a vector containing the set of predictions from all your classifiers for an image, and the target is the image’s class. Train a classifier on
this new training set. Congratulations, you have just trained a blender, and together with the classifiers they form a stacking ensemble! Now let’s evaluate the ensemble on the test set. For each image in the test set, make predictions with all your classifiers, then feed the predictions to the blender to get the ensemble’s predictions. How does it compare to the voting classifier you trained earlier?**

Answer:

