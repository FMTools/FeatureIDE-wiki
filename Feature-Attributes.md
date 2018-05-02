<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < [**Software Product Line Developer**](https://github.com/FeatureIDE/FeatureIDE/wiki/Software-Product-Line-Developer) < [**FeatureIDE Functions in Deep**](https://github.com/FeatureIDE/FeatureIDE/wiki/FeatureIDE-Functions-in-Deep)

<!-- Introduction -->
## Introduction
The **FeatureIDE Attribute View** shows all attributes of the current feature model. The feature model need to be an extended feature model to support the management of attributes. It makes it possible to create and remove attributes from feature. The attributes are saved in a persistent way inside the feature model XML. Additionally, it is also possible to calculate the ranges of attributes for partial configuration using an heuristic.

<!-- Extended Feature Model -->
### 1. Creating an extended feature model
A feature model is called extended feature model if it's features contain attributes. The creation of an extended feature model within FeatureIDE is quite simple.

1. Right-click your procject -> New -> FeatureModel. A wizard opens.
2. Select the name and the related project for the feature model. (see image)

<img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureAttributes/FM_Attributes_CreateEFM_Step2.png" alt="FM_Attributes_CreateEFM_Step2" width=60% height=60%/>

3. Click Next. (not Finish)
4. In the dropdown select the format ExtededFeatureModel. (see image)

<img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureAttributes/FM_Attributes_CreateEFM_Step4.png" alt="FM_Attributes_CreateEFM_Step2" width=60% height=60%/>

5. Click Finish.

<!-- Feature Attribute View -->
### 2. Feature Attribute View
FeatureIDE provides the feature attribute view to support the management of attributes. The view can be opened by clicking on Windows -> Show View -> Other... Now search for 'Feature Attributes' and double click to open the view. 

<!-- Content -->
The functions of the **toolbar** from left to right are:       
