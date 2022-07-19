# FIUBA Dataton 2022 - ZS Employee Churn Prediction Challenge

Busquet Lucas, Hernández Hugo, Iriarte Tomás

We needed to predict whether a certain employee would be terminated next quarter. We began by loading the dataset and cleaning the data. Changing the data types and fixing NaN values. After inspecting the dataset and gaining some insight, we chose certain features and ran a Random Forest Classifier. This did not have a good performance, due to heavily unbalanced classes (Globally 10 Existing to 1 Terminated).

<p align="center">
  <img src="https://user-images.githubusercontent.com/71747228/179608935-7b7f6b42-215b-43c2-83b4-9c8805f294f1.png" />
</p>

Finally we used SMOTE to oversample the minority class, taking care not to leak information into the training set, and re-ran the classifier, obtaining a much better performance.

<p align="center">
  <img src="https://user-images.githubusercontent.com/71747228/179608989-eafc1417-0039-41e9-8c7e-c052da4c1898.png" />
</p>
