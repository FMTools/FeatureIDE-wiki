<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < [**Software Product Line Developer**](https://github.com/FeatureIDE/FeatureIDE/wiki/Software-Product-Line-Developer) < [**FeatureIDE Functions in Deep**](https://github.com/FeatureIDE/FeatureIDE/wiki/FeatureIDE-Functions-in-Deep)

<!-- Introduction -->

<!-- Content -->
<img align="center" alt="feature_model_editor" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureModelEditor.png">

1. **Feature Diagram**  
    Shows the project feature diagram.  
    Here you can add, remove, move, constrain and change the attributes and dependencies of features. You can also export your feature diagram.  
   _Additional shortcuts:_  
    * Change connection types 
        * Double click on connections
    * Rename feature  
        * <kbd>F2</kbd>
    * Insert feature below
        * <kbd>Ins</kbd>
    * Collapse/Expand 
        * <kbd>CTRL</kbd> <kbd>c</kbd>
        * Double click on feature
    * Delete feature or constraint
        * <kbd>Del</kbd>
    * Delete feature including its subtree
        * <kbd>CTRL</kbd> <kbd>d</kbd>
    * Vertical scrolling
        * <kbd>SHIFT</kbd> scroll
    * Zooming in and out
        * <kbd>CTRL</kbd> scroll
        * <kbd>CTRL</kbd> <kbd>+</kbd>
        * <kbd>CTRL</kbd> <kbd>-</kbd>
    * Scrolling
        * Hold middle mouse button and scroll
    * Drag and Drop / Scrolling the Feature Diagram View
        * Hold an element and position your cursor at one of the edges of the Feature Diagram View
    * Select neighboring features
        * <kbd>←</kbd><kbd>↑</kbd><kbd>↓</kbd><kbd>→</kbd> 

2. **Feature Editor Pages**  
   The feature model editor also offers a feature order and a source page. The feature order shows the order of the features when a specific composer is selected. Otherwise the feature order page is blank. The Source page displays the source of the model.xml.  
3. **FeatureIDE Outline**  
   The outline shows the diagram as a tree list. It has the capability to synchronize the visible elements with the feature diagram page. It also shows the constraints.  

4. **Toolbar**  
    * The "Toolbar" is located in the upper right. It provides useful ways to interact with the feature model.
        * ![Alt-Text](./Assets/FeatureModelEditor/Tool%20bar/Tool%20bar.png)
    * The “Search bar” makes it possible to search for features. It also allows the use of regular expressions. After typing search term and pressing “Enter”, the searched feature will be selected. Pressing “Enter” again selects the next feature from the search results.
        * ![Alt-Text](./Assets/FeatureModelEditor/Tool%20bar/Search%20bar.png)
    * “Collapse All” collapses every feature in the diagram. “Expand All” expands every feature in the diagram. “Adjust Model to Editor Size” resizes the diagram to window size by collapsing or expanding the features.  
        * ![Alt-Text](./Assets/FeatureModelEditor/Tool%20bar/CollapseExpand%20bar.png)
    * “Set layout” opens the context menu to change the layout of the diagram. For more information see [here](https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#feature-diagram-layouts).
        * ![Alt-Text](./Assets/FeatureModelEditor/Tool%20bar/Set%20Layout%20bar.png)
    * “Set calculation” opens the context menu to change the calculation of the diagram. For example, these calculations detect redundant cross-tree constraints. This is by default set to "Automatic Calculations", which executes after every change to the feature model. However, for feature models with more than 1000 features we recommend to run these checks on demand and not after every change in the feature diagram.
        * ![Alt-Text](./Assets/FeatureModelEditor/Tool%20bar/Set%20Calculation%20bar.png)

For additional information refer to the corresponding pages under the quick navigation tab.  

<!-- Quick-Navigation-Table -->
### Quick Navigation:
<table>
	<tr>
		<th>
			Feature Diagram
		</th>
		<th>
			Constraint Dialog
		</th>
		<th>
			Feature Order
		</th>
		<th>
			Outline View: Feature Model
		</th>
		<th>
			Coming Soon...
		</th>
	</tr>
	<tr>
		<td width="128px">
			<p align="center">
				<img height="100" width="100" alt="under_construction" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/FeatureDiagramLogo.png">
			</p>
		</td>
		<td width="128px">
			<p align="center">
				<img height="100" width="100" alt="under_construction" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/under_construction.png">
			</p>
		</td>
		<td width="128px">
			<p align="center">
				<img height="100" width="100" alt="under_construction" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/under_construction.png">
			</p>
		</td>
		<td width="128px">
			<p align="center">
				<img height="100" width="100" alt="under_construction" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/under_construction.png">
			</p>
		</td>
		<td width="128px">
			<p align="center">
				<img height="100" width="100" alt="under_construction" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/under_construction.png">
			</p>
		</td>
	</tr>
	<tr>
		<td>
			<p align="center">
				<a href="/FeatureIDE/FeatureIDE/wiki/Feature-Diagram">Feature Diagram</a>
			</p>
		</td>
		<td>
			<p align="center">
				<a href="/FeatureIDE/FeatureIDE/wiki/Constraint-Dialog">Constraint Dialog</a>
			</p>
		</td>
		<td>
			<p align="center">
				<a href="/FeatureIDE/FeatureIDE/wiki/Feature-Order">Feature Order</a>
			</p>
		</td>
		<td>
			<p align="center">
				<a href="/FeatureIDE/FeatureIDE/wiki/Outline-Feature-Model">Outline: Feature Model</a>
			</p>
		</td>
		<td>
			<p align="center">
				<a href="/FeatureIDE/FeatureIDE/wiki/">Coming Soon...</a>
			</p>
		</td>
	</tr>
	<tr>
		<td>
			description follows
		</td>
		<td>
			description follows
		</td>
		<td>
			description follows
		</td>
		<td>
			description follows
		</td>
		<td>
			description follows
		</td>
	</tr>
</table>

For a detailed list of the main functionalities you can have a look at this [screenshots and videos](http://wwwiti.cs.uni-magdeburg.de/iti_db/research/featureide/#screenshots).
<!-- Additonal Content -->
