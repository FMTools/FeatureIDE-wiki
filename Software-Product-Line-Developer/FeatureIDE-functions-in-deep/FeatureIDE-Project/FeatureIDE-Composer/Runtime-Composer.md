<!-- Breadcrumb -->
[**HOME**](https://github.com/tthuem/FeatureIDE/wiki) < **...**  < [**FeatureIDE Project**](https://github.com/tthuem/FeatureIDE/wiki/FeatureIDE-Project) < [**FeatureIDE Composer**](https://github.com/FeatureIDE/FeatureIDE/wiki/FeatureIDE-Composer)

<!-- Introduction -->
##1. Using Run Configurations of Eclipse
###1.1 How to create a RuntimeComposer project of this kind
When creating a new RuntimeComposer project via the New-Project-Wizard, it is set to utilize the Run Configuration method  by default.
For switching from the properties manner to Run Configuration please follow the instructions under (see) except for the fact that you need to change the "Composition Mechanism" reversely.

###1.2 What it does
With this implementation of the RuntimeComposer, the current feature configuration will be read and internally written into the program arguments.

###1.3 User-defined program arguments
The program arguments which you have already set will be considered and not be overwritten.

<img src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureIDEProject/Runtime/run_config.png">


##2. Using properties
###2.1 How to create a RuntimeComposer project of this kind

Since the Run Configuration method (see) is set by default, you have to switch the "Composition Mechanism" from "Run Configurations" to "Properties" to obtain the properties approach.
For this you have to go into Project Properties (right click on the project > Properties) > FeatureIDE > Feature Project > Composition Mechanism  > OK.
After that you need to rebuilt the example project.


###2.2 What it does
This kind of the Runtime Composer reads the current feature configuration and writes it into runtime.properties. 
Every time the project is build runtime.properties will be refreshed.

It contains all available, non-abstract features of the current configuration, while the selected ones are set to true, the unselected ones to false.

<img src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureIDEProject/Runtime/propertyfile_config.png">

###2.3 Getting the values of a property

To get to know whether a certain feature is selected when using the properties method, you can utilize the PropertyManager class which is automatically inserted when creating a new RuntimeComposer of property style. 

Within the PropertyManager there is the getProperty method, returning the values (<code>true</code> or <code>false</code>) of a queried property.

<img src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureIDEProject/Runtime/propertymanager.png">

###2.4 Traceability

In order to find where the getProperty method is called with which feature you can use the FSTModel and the FeatureModel and its color annotations.

###2.4.1 Assigning a color to a feature

see xxx

After that all calls of getProperty with each feature will get the refered color as well as if statements invoking the method.

###2.4.2 Renaming a feature

If a feature is renamed within the model, it will be redefined wherever it is called by the getProperty method.

###2.4.3 Calling getProperty with a non-existing feature

If you call a feature which does not exist in the current feature configuration, a marker will be set in the corresponding line and an error message will be written into the console if the program is executed.

<img src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureIDEProject/Runtime/traceability.png">



