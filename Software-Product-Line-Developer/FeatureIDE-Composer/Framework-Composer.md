<!-- Breadcrumb -->
[**HOME**](https://github.com/tthuem/FeatureIDE/wiki) < **...** < [**FeatureIDE Functions in Deep**](https://github.com/tthuem/FeatureIDE/wiki/FeatureIDE-Functions-in-Deep)  < [**Composer**](https://github.com/tthuem/FeatureIDE/wiki/FeatureIDE-Composer)

<!-- Introduction -->
This composer creates runtime variability using plugins.

There is a subproject inside the feature folder of the main project for each feature. When the main project is build, the composer will automatically build the corresponding JARs containing the binary files and will add the JARs to the classpath of the main project.

<img src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureIDEProject/Framework.png">

The classes inside the feature projects uses interfaces or abstract classes from the source folder inside the main project. Additionally, each feature project contains a file named "info.xml". This file is used for making the different classes inside the jar "visible". If the class is not referenced, it will be ignored during execution.

<img src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureIDEProject/Framework_Subproject.png">