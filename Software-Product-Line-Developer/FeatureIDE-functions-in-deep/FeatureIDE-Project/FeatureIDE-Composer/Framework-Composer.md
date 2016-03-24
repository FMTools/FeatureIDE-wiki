<!-- Breadcrumb -->
[**HOME**](https://github.com/tthuem/FeatureIDE/wiki) < **...**  < [**FeatureIDE Project**](https://github.com/tthuem/FeatureIDE/wiki/FeatureIDE-Project) < [**FeatureIDE Composer**](https://github.com/FeatureIDE/FeatureIDE/wiki/FeatureIDE-Composer)

<!-- Introduction -->
This composer supports frameworks using plugins.

After creation of a new project the composer automatically creates the subprojects for all selected features inside the feature model (1). This includes the "info.xml" that is important for creating the corresponding JARs. The main project provides interfaces and abstract classes that can be used and implemented inside the subprojects (2).
These projects can be checked out and edited in new projects (3).

<img src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureIDEProject/Framework.png">

When saving the configuration of the main project the JARs are build from the feature projects for all selected features. This includes the "info.xml" file containing information about implemented interfaces or extended abstract classes (4). The build JARs are automatically referenced in the framework project (5). Use the PluginLoader to get access to the plugins (6).

The Collaboration Model provides information about all interfaces or abstract classes used in the different features. It also informs the user about the methods or fields containing in all classes referenced inside "info.xml" in each JAR. Overwritten methods inherited from super-classes or interfaces are highlighted.

<img src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureIDEProject/Framework_Model.png">
