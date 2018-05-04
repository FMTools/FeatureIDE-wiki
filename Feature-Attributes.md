<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < [**Software Product Line Developer**](https://github.com/FeatureIDE/FeatureIDE/wiki/Software-Product-Line-Developer) < [**FeatureIDE Functions in Deep**](https://github.com/FeatureIDE/FeatureIDE/wiki/FeatureIDE-Functions-in-Deep)

<!-- Introduction -->
## Introduction
Since release3.5, FeatureIDE supports feature model attributes. The **FeatureIDE Attribute View** shows all attributes of the current feature model. The feature model needs to be an extended feature model to support the management of attributes. The view makes it possible to create and remove attributes from a feature. The attributes are saved in a persistent way inside the feature model XML. Additionally, it is also possible to calculate the ranges of attributes for partial configuration using a heuristic.

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

<img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureAttributes/FM_AttributesView.png" alt="FM_AttributesView" width=49%/>
<img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureAttributes/FM_AttributesView_Table.png" alt="FM_AttributesView_Table.png" width=49%/>

We see the content of the feature attribute view for a simplified extended feature model that represents a car. The feature of the EFM is displayed in a tree that has the same structure as the feature model diagram. 

Now we explain the different operations which are possible with the attribute view:

### 2.1 Create Attributes
FeatureIDE support four different types of attributes: String, Boolean, Long, Double. Attributes can be created by right-clicking a feature and clicking 'Add (String/Boolean..) Attribute'. A new attribute of the selected type with an unique name is created. To change the value, unit, or name of an attribute just double-click their respective cells in the view.
The recursive and configureable states can be switched easily by clicking the checkbox. Note that the type of an attribute cannot be changed after creation.

<img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureAttributes/FM_AttributesView_ADD1.png" alt="FM_AttributesView_Filter.png" width=48%/>
<img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureAttributes/FM_AttributesView_ADD2.png" alt="FM_AttributesView_Filter.png" width=48%/>

### 2.2 Remove Attribute
Right-clicking an attribute open a context-menu with the entry 'Remove feature attribute'. After clicking on the operation the selected attribute is removed.

<img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureAttributes/FM_AttributesView_REMOVE1.png" alt="FM_AttributesView_Filter.png" width=48%/>
<img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureAttributes/FM_AttributesView_REMOVE2.png" alt="FM_AttributesView_Filter.png" width=48%/>

### 2.3 Recursive Attributes
Recursive attributes are inherited to every decendant feature. They can be used to represent attributes for a group of features. Without creating the attribute manually for every descendant. To make an attribute recursive just activate the recursive checkbox. All recursive attributes are then added to the descendants. You can only mark an attribute as recursive when there exists no attribute with the same name on any descendant.

<img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureAttributes/FM_AttributesView_RECURSIVE1.png" alt="FM_AttributesView_Filter.png" width=48%/>
<img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureAttributes/FM_AttributesView_RECURSIVE2.png" alt="FM_AttributesView_Filter.png" width=48%/>

### 2.4 Configurable Attributes and Extended Configurations

The correct management of configurable attributes and the calculation of attribute ranges is currently only available on the branch FeatureIDE/FeatureModel_Attributes.

The value for configurable attributes is set for every specific configuration. Therefore the values are stored in the configuration XML and not inside the feature model XML. The creation of an extended configuration is the same as the feature model but instead of New -> FeatureModel you need to select New -> Configuration and then select the extended configuration as format.

### 2.5 Filtering Attributes
It is possible to filter features and their attributes. To do so activate the sync button on the top right of the view. Now only features and their attributes that are selected in the feature diagram editor are shown in the view. This simplifies the process of searching a certain feature for large feature models. All features that are selected are coloured light green. To contain the tree structure while filtering for features we also show all ancestors of the selected features coloured gray. It is possible to selecte multiple feature in the feature diagram editor.

As an example below we selected the root feature 'Car' in the feature diagram editor. Therefore, only 'Car' and it's attributes are shown.

<img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureAttributes/FM_AttributesView_Filter.png" alt="FM_AttributesView_Filter.png" width=60% height=60%/>
    
