# ML-models-for-CO2-Reduction
Metals Catalysts with ZnSe

Machine learning (ML) modeling is becoming increasingly popular in chemistry research due to its ability to make successful predictions and application flexibility in a variety of physical systems. Based on the previous success of Reisner et al, we created a series of ML models to predict the best transition metal molecular catalysts for our CO2  reduction system, consisting of ZnSe quantum dots (QDs), sodium ascorbate, and transition metals in the aqueous environment.  

Our previous transition metal database, composed of metals from 0.1 to 1000 uM, served as a dataset for training our ML models where the CO amount produced was chosen as a target. In order to improve their accuracy, different features were implemented, such as extinction coefficient, maximum absorption wavelength, reduction potentials, electronegativity etc. Additionally, the dataset was preprocessed through the implementation of dimensionality reduction and standardization which further benefited the performance of our models.

The main models implemented were decision tree regressor (DTR), random forest regressor (RFR), and extreme gradient boosting regressor (XGB) that were all trained on 70% of the dataset and tested on the remaining 30%. All models belong to the category of supervised regression models which break out the training set into smaller subsets and train a multitude of decision trees that either make a mean prediction or serve as a parent to the next set of decision trees, each correcting errors made by the previous ones. Based on the prediction of CO content and the actual value in the test set, the models’ accuracies were estimated by root mean square value and R2. Additionally, Shapley Additive explanations (SHAP) were used to provide insights into how each feature contributes to the model's predictions. 

As a result, RFR achieved the highest R2 with the value of 0.784, indicating a good performance of the model, especially for a physical system with a small dataset (~100 labels/entries). The difference between the predicted and the true values you can see on the following figure where the x-axis are different data entries and the y-axis is a standardized output value - the amount of CO produced. 

Finally,  by utilizing the SHAP values of the RFR model, we made a prediction for each transition metal in the periodic table that strongly indicated the preference for the noble and heavy metals, such as Ir, Au, W, Pt, Ag etc. 
In the future, these metals will be tested to verify the predictions of our model as well as to improve it by expanding the dataset with new entries.  



