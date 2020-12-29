**Machine Learning for prediction of the RMSD (Root Mean Square Deviation) of a decoy set using Physicochemical Properties of Protein Tertiary Structure Data Set**

The workflow followed here is adapted from the book [Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow](https://g.co/kgs/bvvihi) by **Aurélien Geron**.

*The dataset is downloaded from this link [Physicochemical Properties of Protein Tertiary Structure Data Set](https://archive.ics.uci.edu/ml/datasets/Physicochemical+Properties+of+Protein+Tertiary+Structure).* 

*This notebook is divided into two sections:*
1. **Data preprocessing** *- Explore the dataset and prepare it before regression*
2. **Model selection, training and fine tuning** *- Try with various models, compare their performance and fine tune them*

So far, we have walked through the following steps:
* Data Preprocessing:
 * Data visualization - Correlations plots, Bar charts etc.
 * Train test split - Stratified Sampling
 * Scaling - Standard scaling
 * Dimensionality Reduction - PCA with 99% explained variance 
* Model Selection:
 * Linear Model 
 * Random Forest Regressor
 * Artificial Neural Networks
 * GridSearch for better hyperparameters selection
 
Now we need to think about which model to choose between all the ones we analysed. Let us start with comparing the accuracy of each model to begin with:

|Model |Mean RMSE score|
|------|:---------:|
|Linear Model| 0.3|
|Random Forest Regressor | 0.3|
|Artificial Neural Network (ANN) | 0.3|

At this point, we can conclude the following:
* The Linear Regression model is very fast to compute but suffers from low accuracy
* Random Forest Regressor and Artifical Neural Network (ANN) both perform better than Linear Regression model and one of these should be chosen as a suitable model
* The specific model to be chosen for this is a tradeoff between:
 * Speed of prediction **vs** Accuracy
 * Computational resources available at prediction stage **vs** model complexity
 * Model updation considerations
 * Explainability
* We need to adapt the decision based on more information of the deployment platform