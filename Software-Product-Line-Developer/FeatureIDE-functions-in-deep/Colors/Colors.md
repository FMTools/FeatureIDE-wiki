<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < [**Software Product Line Developer**](https://github.com/FeatureIDE/FeatureIDE/wiki/Software-Product-Line-Developer) < [**FeatureIDE Functions in Deep**](https://github.com/FeatureIDE/FeatureIDE/wiki/FeatureIDE-Functions-in-Deep)

<!-- Introduction -->

An example of how to colorate an AHEAD project.

<!-- Outline -->
1. [How to manipulate Color Schemes] (#1-how-to-manipulate-color-scheme)
	1. [Create New Color Scheme] (#1i-create-new-color-scheme)
	2. [Rename Color Scheme] (#1ii-rename-color-scheme)
	3. [Delete Color Scheme](#1iii-delete-color-scheme)
    4. [Change Color Scheme] (#1iv-change-color-scheme)
2. [Coloration](#2-coloration)
  1. [Coloration Menu Point](#2i-coloration-menu-point)
        1. [Feature Diagram](#2ia-feature-diagram)
        2. [FeatureIDE Outline](#2ib-featureide-outline)
        3. [Collaboration Diagram](#2ic-collaboration-diagram)
        4. [Highlighting of composed FOP files](#2id-highlighting-of-composed-fop-files)
        5. [Configuration Map](#2ie-configuration-map)
  2. [Coloration Dialog](#2ii-coloration-dialog)
3. [Results of the Coloration](#3-results-of-the-coloration)
	1. [Feature DiagramEditor](#3i-feature-diagrameditor)
	2. [Collaboration Diagram](#3ii-colaboration-diagram)
	3. [FeatureIDE Outline](#3iii-featureide-outline)
	4. [Project Explorer](#3iv-project-explorer)
	5. [Annotations and Highlighting](#3v-annotations-and-highlighting)
	6. [Configuration Tree/Advanced Configuration Tree](#3vi-configuration-tree/advanced-configuration-tree)
  7. [Configuration Map](#3vii-configuration-map)


<!-- Content -->
## 1. How to manipulate Color Schemes

### 1.i. Create new Color Scheme
_**This part has already been updated for version 3.3.**_ 
 
You have two options to create a new Color Scheme, if there is none selected or none created. Otherwise just **Method 1** will work.
This is necessary to color a feature because the **default** profile is not able to apply colors and is therefore used for statistics and calculations.
		
**Method 1**:
 
Rightclick on a FeatureProject to get into the FeatureIDE menu.

![Add Color Scheme](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/AddColorScheme.png)
		
Click "**Add Color Scheme**" to add a new Color Scheme.
		
![Name New Color Scheme](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/NameNewColorScheme.png)
 
**Method 2**:
 
(This method will only work, if you haven’t created a Color Scheme or haven’t selected one.)
 
Rightclick on a Feature in the Feature Diagram to open the Context Menu and use the menu point "**Feature Color**".
 
![Add Color Scheme In Feature Diagram](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/AddColorSchemeInFeatureDiagram.png)
 
This will open a dialog, where you can either select an existing Color Scheme or create a new one.
 
![Create Color Scheme](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/CreateColorScheme.png)
 
![Select Or Create Color Scheme](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/SelectOrCreateColorScheme.png)
		
### 1.ii. Rename Color Scheme

To rename a Color Scheme you first have to select the Color Scheme, you want to rename. Then open the FeatureIDE menu as shown above.
If you click "**Change Name**" you can rename your profile.
		
![New Name](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/NewName.png)
		
### 1.iii. Delete Color Scheme

Open the FeatureIDE menu as shown above. If you click on "**Delete Color Scheme**" you will delete your profile and the active profile will be set to **default**. (This only works, if a Color Scheme is selected.)
	
### 1.iv. Change Color Scheme
_**This part has already been updated for version 3.3.**_
    
Open the FeatureIDE menu as shown above. You can choose the Color Scheme by clicking on it.
 
![Change Color Scheme](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ChangeColorScheme.png)
    	
## 2. Coloration
		
### 2.i. Coloration Menu Point

#### 2.i.a Feature Diagram
 
_**This part has already been updated for version 3.3.**_
 
Rightclick on a feature in the FeatureDiagram to open the ContextMenu and use the menu point “**Feature Color**” as shown below.
 
![Feature Diagram Menu](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/FeatureDiagramMenu.png)
 
If there is no Color Scheme created or selected, you can create or select one.
 
#### 2.i.b FeatureIDE Outline
 
_**This part has already been updated for version 3.3.**_
 
Rightclick on a feature in the FeatureIDE Outline to open the Context Menu and use the menu point “**Feature Color**” as shown below.
 
![Tree Outline Menu](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/TreeOutlineMenu.png)
 
![Antenna Outline Menu](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/AntennaOutlineMenu.png)
 
#### 2.i.c Collaboration Diagram
 
_**This part has already been updated for version 3.3.**_
 
Rightclick on a feature in the Collaboration Diagram to open the Context Menu and use the menu point “**Feature Color**” as shown below.
 
![Collaboration Diagram Menu](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/CollaborationDiagramMenu.png)
 
If you rightclick on a class, the menu point “**Feature Color**” won’t be shown, because there is no option to colorize a class.
 
![Collaboration Diagram Menu Without Color](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/CollaborationDiagramMenuWithoutColor.png)
 
#### 2.i.d Highlighting of composed files for FOP
 
_**This part has already been updated for version 3.3.**_
 
Select a module by clicking in the code, then rightclick to open the Context Menu and use the menu point “**Feature Color**” as shown below.
 
![Highlighting Menu](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/HighlightingMenu.png)
 
**Caution:** If the cursor is positioned in a module and the rightclick occurs on an other module, the module, where the cursor is, will be colored.
 
You can enable and disable the highlighting in the editor by opening the Context Menu and using the menu point “**Enable Editor Highlighting**”.

![Highlighting Menu Enable](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/HighlightingMenuEnable.png)

#### 2.i.e Configuration Map
 
Under construction.
		
### 2.ii. Coloration Dialog
_**This part has already been updated for version 3.3.**_

If a Color Scheme is selected, a Coloration Dialog will open. Otherwise you can create a new Color Scheme. 

![Coloration Dialog](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ColorationDialog.png)
		 
The Coloration Dialog offers two important options. 
		 
* **Action**: As shown below you can choose one of those actions. 
		 
![Choose Action](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ChooseAction.png)
		  
* **Color**: You can choose one of ten baseline colors.
		 
![Choose Color](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ChooseColor.png)
		 
In the preview you see the visualization of the colored features.
		 
![Preview](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/Preview.png)
		 
If you press "**OK**" the selected features will be colored. 
If you press "**Cancel**" changes will be discarded.
    
If the selected feature already has a color, it will be shown in the dialog.
 
![ColoredFeature](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ColoredFeature.png)
		 
## 3. Results of the Coloration

Overview of the colored views in Eclipse.
 
![Colored Results](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ColoredResults.png)
		
###3.i. Feature DiagramEditor

Colored features in the Feature DiagramEditor.
 
![Colored Feature Diagram](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ColoredFeatureDiagram.png)

###3.ii. Collaboration Diagram

Colored features in the Collaboration Diagram. (The feature "Wonderful" is not shown, because it is not included in this configuration.)
 
![Colored Beautiful World](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ColoredBeautifulWorld.png)

###3.iii. FeatureIDE Outline

Colored features in the FeatureIDE Outline as shown when the Feature Diagram is opened.
 
![Colored Outline](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ColoredOutline.png)
 
Colored features in the FeatureIDE Outline as shown when a java-file for an example of an Antenna project is opened. 
 
![Colored Outline Antenna](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ColoredOutlineAntenna.png)
 
###3.iv. Project Explorer

A general overview how the colored Project Explorer looks. (For example a Feature House Project)
 
![Colored Project Explorer FH](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ColoredProjectExplorerFH.png)
 
Munge and Antenna projects do not have feature folders. The preview which kind of feature is included in which file or folder is only shown in the build folder but Munge also shows them in the source folder.

![Colored Project Explorer Antenna](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ColoredProjectExplorerAntenna.png)

###3.v. Annotations and Highlighting

Highlighting of composed files for FOP. Colors show from which module each method and fiels comes from. (For example a Feature House project)
 
![Colored Highlighting FH](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ColoredHighlightingFH.png)

Annotations in the feature files.
 
![Colored Annotations FH](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ColoredAnnotationsFH.png)
 
The highlighting looks a bit different in Antenna projects.
 
![Colored Highlighting Antenna](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ColoredHighlightingAntenna.png)
 
###3.vi. Configuration Tree/Advanced Configuration Tree		

Colored features in the Configuration Tree of the chosen configuration.
 
![Colored Configuration Tree](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ColoredConfigurationTree.png)

Colored features in the Advanced Configuration Tree of the chosen configuration.
 
![Colored Advanced Configuration Tree](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ColoredAdvancedConfigurationTree.png)
 
###3.vii Configuration Map
 
Colored features in the Configuration Map. (Under construction.)