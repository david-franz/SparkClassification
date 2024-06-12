# Predicting Malware Class of Android Apps Based on Network Traffic Features

In this project, the goal is to develop a machine learning model capable of detecting whether an Android application is malware or not, based on features extracted from network traffic data. This involves several key steps including data pre-processing, feature engineering, model training, evaluation, and comparison of different model configurations.

## Details of Input Data

• **Data Source:** The dataset used for this task is from Kaggle- the Android Malware Detection dataset. This dataset contains a variety of network traffic data relevant to Android malware detection. The dataset was slightly processed (to remove spaces in the column names), and the processed dataset can be downloaded here: https://archive.org/download/android-malware

• **Data Size:** This dataset is approximately 200MB.

• **Original Number of Features:** The original dataset comprises of 83 features. In our project,
we use a filter feature selection to bring the input data feature size to 30.

• **Instances:** The 83 features represent various bits of data about network traffic. The instances
themselves are labelled one of four classes: Android_Adware (147443 instances),
Android_Scareware (117082), Android_SMS_Malware (67397) and Benign (23708).

• **Feature Types:** The features in the dataset are of mixed types:
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;o NumericalFeatures:Quantitativeattributessuchasportnumbers.
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;o CategoricalFeatures:Qualitativeattributessuchasflags.

• **Missing Values:** Some features have missing values (null) for some of their data entries. For
these, we replace the null values for 0.0.

## Expected Output

The primary objective is to build a trained machine learning model that can accurately classify network connections as one of the four classes based on the extracted features. The performance of the model will be evaluated using metrics such as accuracy on both the training and test datasets. The specific outputs include:

• **Model:**
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;o A trained Random Forest classifier capable of making predictions based on network traffic features. Four different possible classes.
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;o Create several models for using normalisation and PCA or not. Four different models in total with different pipelines setup.

• **Accuracy Metrics:**
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;o **Training Accuracy:** The accuracy of the model on the training dataset, indicating how well the model has learned from the training data.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;o **Test Accuracy:** The accuracy of the model on the test dataset, indicating the model’s generalization ability to unseen data.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;o **Run Times:** The time taken to train and evaluate the model in each run, providing an understanding of the computational efficiency of the different model configurations.
   
• **Statistical Measures:**
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;o **Minimum, Maximum, Average Accuracy:** Metrics to capture the range and central tendency of the model’s performance across multiple runs.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;o **Standard Deviation of Accuracy:** A measure of the variability in the model’s performance, providing insights into the consistency of the model.

![average_accuracy](https://github.com/david-franz/Spark_Android-Malware-Detector/assets/52574893/f0c17c29-2b5c-444e-adb1-04c2d5a5254c)

![average_run_times](https://github.com/david-franz/Spark_Android-Malware-Detector/assets/52574893/7a3c9d22-b0eb-4d41-8967-81477ffef8c4)

![correlatation_coefficients](https://github.com/david-franz/Spark_Android-Malware-Detector/assets/52574893/5eb47484-a4ee-4b5a-a692-908ea582c5a1)


