The **statistic view** for FeatureIDE-projects displays general information about a FeatureIDE project (the project of the current file in the editor). The statistics contain information about the feature model, the implementation, and the specification of the product line. 

The toolbar of the view provides a button to refresh ![refresh button](https://raw.githubusercontent.com/tthuem/FeatureIDE/master/plugins/de.ovgu.featureide.ui/icons/refresh_tab.gif) and one ![export button](https://raw.githubusercontent.com/tthuem/FeatureIDE/master/plugins/de.ovgu.featureide.ui/icons/export_wiz.gif) to export the information to a “*.cvs” file. 

[ ![statistic view image]( http://i.imgur.com/Xi96sVK.png) ](http://i.imgur.com/Xi96sVK.png)
(FeatureIDE Statistics: example)


## 1 Statistics of the feature model

General information about the feature-model.

## 2 Statistic of product- line implementation

Double-click to the main-node opens the detailed tree. 

The first node in the line informs about the number of the classes (also supported nested classes) and roles in this project. Double-click on this Node expands the sub-nodes, which display the package and the name of these classes and their number of roles. On double-click again the next sub-node-level expands and shows the name of these roles, double-click on these names will open the file and jumps to the first line of the editor to edit the class.

The second and the third node works similar. The first part shows the unique names, which will be expanded on the next tree-level. The second-part count the whole number of fields respectively methods and inform about the double-named. 
The second will expand on the first double-click. If expanded, clicking on this node again sort the Objects in alphabetical or descending order.
In addition to the features of the class-node, the field-node and the method-node shows there type respectively the type of the parameter and the return-value-type. 

The fourth node displays the lines of code (LOC) sorted by extensions or features. In expanded state the extension-node informs about LOC in existing extensions in the project (with LOC- no images!) in sum and on the next level in detail. The feature-node works analogue. By double-click again on the expanded node the sub-nodes are sortable by alphabetical or descent order. 
Recently following extensions ignore comments for LOC-counting: java, c, h, jj, jak, cs. Default solution only counts the lines of code without spaces and empty lines. 

[![implementation example]( http://i.imgur.com/SlHKcGk.png)](http://i.imgur.com/SlHKcGk.png)

## 3 Statistic of product- line specification

It shows detailed information about the invariants and the methods of project which implements these features. 

The first node is about the invariants in classes. It delivers the package and the feature of the invariant and the names of them. Double-click on the name and the editor will open and the cursor jumps to the line of interest.

The second and third nodes are about contracts and work analogue.

The fourth node shows the number of all explicit contract refinements.

The fifth node shows the method contracts sorted by feature.

[![specification example](http://i.imgur.com/QWGNgtk.png)](http://i.imgur.com/QWGNgtk.png)


 



