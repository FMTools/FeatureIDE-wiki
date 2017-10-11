<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < [**Software Product Line Developer**](https://github.com/FeatureIDE/FeatureIDE/wiki/Software-Product-Line-Developer) < [**FeatureIDE Functions in Deep**](https://github.com/FeatureIDE/FeatureIDE/wiki/FeatureIDE-Functions-in-Deep)

<!-- Introduction -->
The **statistic view** for FeatureIDE-projects displays general information about a FeatureIDE project (the project of the current file in the editor). The statistics contain information about the feature model, the implementation, and the specification of the product line. 

<!-- Outline -->
1. [Statistics of the feature model] (#1-statistics-of-the-feature-model)
2. [Statistic of product-line implementation] (#2-statistic-of-product-line-implementation)
3. [Statistic of product-line specification] (#3-statistic-of-product-line-specification)

<!-- Content -->
The toolbar of the view provides a button to refresh ![refresh button](https://raw.githubusercontent.com/FeatureIDE/FeatureIDE/master/plugins/de.ovgu.featureide.ui/icons/refresh_tab.gif) and one ![export button](https://raw.githubusercontent.com/FeatureIDE/FeatureIDE/master/plugins/de.ovgu.featureide.ui/icons/export_wiz.gif) to export the information to a “*.cvs” file. 

![Example](https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/StatisticsView/example.png)

## 1 Statistics of the feature model

General information about the feature-model. Such as number of features and number of valid configurations.

## 2 Statistic of product-line implementation

The first node in the line informs about the number of the **classes** (including nested classes) and roles. The child nodes show the different classes and files of the product line. The number of each node indicates how often the class is refined. The child of these classes show the corresponding features; the corresponding files can be opened via double-click. 

The second node shows statistics about **fields** and the third about **methods**. The number of unique methods contains only method resp. field introductions, thus each element is counted only once. The first part shows the unique names, which will be expanded on the next tree-level. The second-part count the whole number of fields respectively methods. Double clicking on the root node for features respectively methods sort the Objects in alphabetical or descending order. 

_**This part has already been updated for version 3.3.**_ 

The fourth node(in preprocessor projects the third node) displays the **Lines Of Code** (LOC). The sub-nodes order the lines of code for all composer types by file extension. Additionally for preprocessor projects it will count the LOC by features, non-variable code, variable code and preprocessor statements. The subentries can be sorted alphabetically or in descending order via double-click.
Comments are not counted for the following file extensions: java, c, h, jj, jak, and cs. The default solution LOC counting only counts the lines of code without spaces and empty lines. 

<td width="350px"> <p align="center">
<img height="450px" alt="under construction" src="https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/FeatureHouseImport/StatisticsViewSimple.png">
<img height="450px" alt="under construction" src="https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/FeatureHouseImport/StatisticsViewFull.png">
<br> The left image shows the composer independent view and the right image shows the special LOCs for preprocessor projects.
</p></td>

## 3 Statistic of product-line specification

It shows detailed information about the specification of the product line. Currently only for feature-oriented contracts in JML with FeatureHouse. 

The first node shows statistics about **invariants**. The sub-nodes show detailed information on ionvariants for each class.

The second and third nodes show statistics about **contracts** and **methods with contracts** work analogue.

The fourth node shows statistics about the usage of **contract refinement strategies**.

The fifth node shows details on **method contracts**.

![Example](https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/StatisticsView/specification.png)


 


