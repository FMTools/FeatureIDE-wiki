The **statistic view** for FeatureIDE-projects displays general information about a FeatureIDE project (the project of the current file in the editor). The statistics contain information about the feature model, the implementation, and the specification of the product line. 

The toolbar of the view provides a button to refresh ![refresh button](https://raw.githubusercontent.com/tthuem/FeatureIDE/master/plugins/de.ovgu.featureide.ui/icons/refresh_tab.gif) and one ![export button](https://raw.githubusercontent.com/tthuem/FeatureIDE/master/plugins/de.ovgu.featureide.ui/icons/export_wiz.gif) to export the information to a “*.cvs” file. 

![Example](https://github.com/tthuem/FeatureIDE/wiki/Assets/StatisticsView/example.png)

## 1 Statistics of the feature model

General information about the feature-model. Such as number of features and number of valid configurations.

## 2 Statistic of product-line implementation

The first node in the line informs about the number of the **classes** (including nested classes) and roles. The child nodes show the different classes and files of the product line. The number of each node indicates how often the class is refined. The child of these classes show the corresponding features; the corresponding files can be opened via double-click. 

The second node shows statistics about **fields** and the third about **methods**. The number of unique methods contains only method resp. field introductions, thus each element is counted only once. The first part shows the unique names, which will be expanded on the next tree-level. The second-part count the whole number of fields respectively methods. Double clicking on the root node for features respectively methods sort the Objects in alphabetical or descending order. 

The fourth node displays the **Lines Of Code** (LOC). The sub-nodes orde the lines of code by file extension and feature. The subentries can be sorted alphabetically or in descending order via double-click.
Comments are not counted for the following file extensions: java, c, h, jj, jak, and cs. The default solution LOC counting only counts the lines of code without spaces and empty lines. 

![Example](https://github.com/tthuem/FeatureIDE/wiki/Assets/StatisticsView/implementation.png)

## 3 Statistic of product-line specification

It shows detailed information about the specification of the product line. Currently only for feature-oriented contracts in JML with FeatureHouse. 

The first node shows statistics about **invariants**. The sub-nodes show detailed information on ionvariants for each class.

The second and third nodes show statistics about **contracts** and **methods with contracts** work analogue.

The fourth node shows statistics about the usage of **contract refinement strategies**.

The fifth node shows details on **method contracts**.

![Example](https://github.com/tthuem/FeatureIDE/wiki/Assets/StatisticsView/specification.png)


 


