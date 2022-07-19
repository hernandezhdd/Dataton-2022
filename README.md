# FIUBA Dataton 2022 - ZS Employee Churn Prediction Challenge

<b>Busquet Lucas, Hernández Hugo, Iriarte Tomás</b>

We needed to predict whether a certain employee would be terminated next quarter. We began by loading the dataset and cleaning the data. Changing the data types and fixing NaN values. After inspecting the dataset and gaining some insight, we plotted the next figures:

<p align="center">
  <b>Time in the company</b>
</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/71747228/179814256-0b2e5f68-6dc7-404f-af78-1748f7d003e1.png"
  width="500" />
</p>

<p align="center">
  <b>GeoMatch: Whether an employee lived in the same city as his manager</b>
</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/71747228/179814810-8c8fccb4-4fbf-44d1-84ee-87c5e0b02d59.png"
  width="500" />
</p>

<p align="center">
  <b>Terminated employees by sales amount</b>
</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/71747228/179815174-deb76d01-c127-421d-b356-a1419bb031cf.png"
  width="500" />
</p>


<p align="center">
  <img src="https://user-images.githubusercontent.com/71747228/179815377-498ccadd-19cf-48d0-8553-504031905760.png"
  width="500" />
</p>

With those and other important features we ran a Random Forest Classifier. This did not have a good performance, due to heavily unbalanced classes (Globally 10 Existing to 1 Terminated). 

<p align="center">
  <img src="https://user-images.githubusercontent.com/71747228/179608935-7b7f6b42-215b-43c2-83b4-9c8805f294f1.png" />
</p>

Finally we used SMOTE to oversample the minority class, taking care not to leak information into the training set, and re-ran the classifier, obtaining a much better performance.

<p align="center">
  <img src="https://user-images.githubusercontent.com/71747228/179608989-eafc1417-0039-41e9-8c7e-c052da4c1898.png" />
</p>


<p align="center">
  <b>Image of the dashboard</b>
</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/71747228/179818556-727e93d2-c2a1-4434-8837-a3067431ffc9.jpeg" />
</p>

