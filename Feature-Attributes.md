<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < [**Software Product Line Developer**](https://github.com/FeatureIDE/FeatureIDE/wiki/Software-Product-Line-Developer) < [**FeatureIDE Functions in Deep**](https://github.com/FeatureIDE/FeatureIDE/wiki/FeatureIDE-Functions-in-Deep)

<!-- Introduction -->
## Introduction
The **FeatureIDE Attribute View** shows all attributes of the current feature model. The feature model needs to be an extended feature model to support the management of attributes. It makes it possible to create and remove attributes from a feature. The attributes are saved in a persistent way inside the feature model XML. Additionally, it is also possible to calculate the ranges of attributes for partial configuration using a heuristic.

<!-- Extended Feature Model -->
## 1. Creating an Extended Feature Model
A feature model is called extended feature model if it features contain attributes. The creation of an extended feature model within FeatureIDE is quite simple.

1. Right-click your project -> New -> FeatureModel. A wizard opens.
2. Select the name and the related project for the feature model. (see image)

<img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureAttributes/FM_Attributes_CreateEFM_Step2.png" alt="FM_Attributes_CreateEFM_Step2" width=60% height=60%/>

3. Click Next. (not Finish)
4. In the drop-down select the format ExtededFeatureModel. (see image)

<img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureAttributes/FM_Attributes_CreateEFM_Step4.png" alt="FM_Attributes_CreateEFM_Step2" width=60% height=60%/>

5. Click Finish.

<!-- Feature Attribute View -->
## 2. Feature Attribute View
FeatureIDE provides the feature attribute view to support the management of attributes. The view can be opened by clicking on Windows -> Show View -> Other... Now search for 'Feature Attributes' and double-click to open the view. 

<img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureAttributes/FM_AttributesView.png" alt="FM_AttributesView" width=60% height=60%/>
<img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureAttributes/FM_AttributesView_Table.png" alt="FM_AttributesView_Table.png" width=60% height=60%/>
<img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureAttributes/FM_AttributesView_Filter.png" alt="FM_AttributesView_Filter.png" width=60% height=60%/>

We see the content of the feature attribute view for a simplified extended feature model that represents a car. The feature of the EFM is displayed in a tree that has the same structure as the feature model diagram. Every entry with a blue 'f' icon is a feature. His attributes are directly listed below and have either an 'a' or 'r' as an icon.  

Now we explain the different operation which is possible with the attribute view:

### 2.1 Create Attributes
FeatureIDE support four different types of attributes: String, Boolean, Long, Double. 

### 2.2 Remove Attribute
### 2.3 Recursive Attributes
### 2.4 Configurable Attributes
    
