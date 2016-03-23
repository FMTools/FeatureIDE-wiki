<!-- Breadcrumb -->
[**HOME**](https://github.com/tthuem/FeatureIDE/wiki) < **...**  < [**FeatureIDE Project**](https://github.com/tthuem/FeatureIDE/wiki/FeatureIDE-Project) < [**FeatureIDE Composer**](https://github.com/FeatureIDE/FeatureIDE/wiki/FeatureIDE-Composer)

<!-- Introduction -->
This composer creates runtime variability using plugins.

There is a subproject inside the feature folder of the main project for each feature. When the main project is build, the composer will automatically build the corresponding JARs containing the binary files and will add the JARs to the classpath of the main project.

<img src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureIDEProject/Framework.png">

The classes inside the feature projects use interfaces or abstract classes from the source folder inside the main project. Additionally, each feature project contains a file named "info.xml". This file is used for making the different classes inside the jar "visible". If the class is not referenced, it will be ignored during execution.

<img src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureIDEProject/Framework_Subproject.png">

The Collaboration Model provides information about all interfaces or abstract classes used in the different features. It also informs the user about the methods or fields containing in all classes referenced inside "info.xml" in each JAR. Overwritten methods inherited from super-classes or interfaces are highlighted.

<img src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureIDEProject/Framework_Model.png">
