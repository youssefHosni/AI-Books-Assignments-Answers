### Questions ###

[1. What are the main motivations for reducing a dataset’s dimensionality? What are the main drawbacks?]()

[2. What is the curse of dimensionality?]()

[3. Once a dataset’s dimensionality has been reduced, is it possible to reverse the operation? If so, how? If not, why?]()

[4. Can PCA be used to reduce the dimensionality of a highly nonlinear dataset?]()

[5. Suppose you perform PCA on a 1,000-dimensional dataset, setting the explained variance ratio to 95%. How many dimensions will the resulting dataset have?]()

[6. In what cases would you use vanilla PCA, Incremental PCA, Randomized PCA, or Kernel PCA?]()

[7. How can you evaluate the performance of a dimensionality reduction algorithm on your dataset?]()

[8. Does it make any sense to chain two different dimensionality reduction algorithms?]()

[9. Load the MNIST dataset (introduced in Chapter 3) and split it into a training set and a test set (take the first 60,000 instances for training, and the remaining
10,000 for testing). Train a Random Forest classifier on the dataset and time how long it takes, then evaluate the resulting model on the test set. Next, use PCA to
reduce the dataset’s dimensionality, with an explained variance ratio of 95%. Train a new Random Forest classifier on the reduced dataset and see how long it
takes. Was training much faster? Next evaluate the classifier on the test set: how does it compare to the previous classifier?]()

[10. Use t-SNE to reduce the MNIST dataset down to two dimensions and plot the result using Matplotlib. You can use a scatterplot using 10 different colors to represent each image’s target class. Alternatively, you can write colored digits at the location of each instance, or even plot scaled-down versions of the digit images
themselves (if you plot all digits, the visualization will be too cluttered, so you should either draw a random sample or plot an instance only if no other instance
has already been plotted at a close distance). You should get a nice visualization with well-separated clusters of digits. Try using other dimensionality reduction
algorithms such as PCA, LLE, or MDS and compare the resulting visualizations.]()

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Answers ###

1. What are the main motivations for reducing a dataset’s dimensionality? What are the main drawbacks?

Answer:
* Increase the training speed or decrease the time complexity.
* Remove the unneeded informatino which might affect the training and model performance which is known as the curise of dimensiionality 
* To be able to visualize the data. 
* Saving storage/meomery space. 

**Some of the drawbacks:** 

* Increase the machine learning pipeline complexity 
* Depending on the training dataset size this might take alot of time and computation power
* It is alawys diffuilt to explain the results with a transformed features. 

2. What is the curse of dimensionality?

Answer:

Curse of dimensionality occurs when the data has large number of dimension and small data size so the distance between each instance will be large and the data will be sparse. This will therfore will make the model diffuiclt to capture the pattern in the data a model is trained on this data. Also it increase the risk of  overfitted on the training data and if a new instance is added it will be probably away from the other instances and the moedl will not be able to predict its value or classify it right. 

3. Once a dataset’s dimensionality has been reduced, is it possible to reverse the operation? If so, how? If not, why?

Answer:

It depends on the data itself and the way you applied the dimensionality reduction to it. For example PCA is used then we can revesre the data and obtain almost the data. However it is important to ensure that the data can not be obtained perfectly since part of the data will be lost during the transformation. This part depends on how many percentage did the chosen component did cover and the rest will be lost. 

4. Can PCA be used to reduce the dimensionality of a highly nonlinear dataset?

Answer:
Yes PCA can be used to reduce the dimension of a highly nonlinear datasets however if they are for example swiss roll dataset it will lead to losing alot of information since your goal in this case should be unroll it not squashing it. 

5. Suppose you perform PCA on a 1,000-dimensional dataset, setting the explained variance ratio to 95%. How many dimensions will the resulting dataset have?

Answer:
It depends on the dataset itself.


6. In what cases would you use vanilla PCA, Incremental PCA, Randomized PCA, or Kernel PCA?

Answer:
* vanilla PCA: The tradional PCA which is used if the data fit in the meomery and not very strong non linear datasets. 
* Incremental PCA: This will be a good choice if you have large dataset that cannot fit the meomery 
* Randomized PCA: This can be used to decrease the computation time as they find an approximation of the first d components.
* Kernel PCA: It is useful for non linear dataset

7. How can you evaluate the performance of a dimensionality reduction algorithm on your dataset?

Answer:

In genral the dimensionality reduction algorithm will work well if it reduce the dimension and in the same time did not loss any important informatino. This can be measured in two ways depending on the algorithm. If the algorithm can reverse the data then we can measure the distance between the reversed data set and the orignal dataset. If it can not then another method will be by using an predictive algorithm and measure the perfomrance of the model before and after dimensionality reduction.

8. Does it make any sense to chain two different dimensionality reduction algorithms?

Answer:
Yes, For example we can use PCA for first remove large number of uneeded usless dimension then use LLE to remove more dimension. This will be similar to use LLE but in fraction of time.  

9. Load the MNIST dataset (introduced in Chapter 3) and split it into a training set and a test set (take the first 60,000 instances for training, and the remaining
10,000 for testing). Train a Random Forest classifier on the dataset and time how long it takes, then evaluate the resulting model on the test set. Next, use PCA to
reduce the dataset’s dimensionality, with an explained variance ratio of 95%. Train a new Random Forest classifier on the reduced dataset and see how long it
takes. Was training much faster? Next evaluate the classifier on the test set: how does it compare to the previous classifier?

Answer:



10. Use t-SNE to reduce the MNIST dataset down to two dimensions and plot the result using Matplotlib. You can use a scatterplot using 10 different colors to represent each image’s target class. Alternatively, you can write colored digits at the location of each instance, or even plot scaled-down versions of the digit images
themselves (if you plot all digits, the visualization will be too cluttered, so you should either draw a random sample or plot an instance only if no other instance
has already been plotted at a close distance). You should get a nice visualization with well-separated clusters of digits. Try using other dimensionality reduction
algorithms such as PCA, LLE, or MDS and compare the resulting visualizations.

Answer:


