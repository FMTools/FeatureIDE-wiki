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
	2. [Coloration Dialog](#2ii-coloration-dialog)
3. [Results of the Coloration](#3-results-of-the-coloration)
	1. [Feature DiagramEditor](#3i-feature-diagrameditor)
	2. [Collaboration Diagram](#3ii-colaboration-diagram)
	3. [FeatureIDE Outline](#3iii-featureide-outline)
	4. [Project Explorer](#3iv-project-explorer)
	5. [Annotations and Highlighting](#3v-annotations-and-highlighting)
	6. [Configuration Tree/Advanced Configuration Tree](#3vi-configuration-tree/advanced-configuration-tree)


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
 
![Add Feature Color In Feature Diagram](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/AddFeatureColorInFeatureDiagram.png)
 
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

Rightlick on FeatureDiagramm to open the ContextMenu and use the menu point as shown below.
		
![Coloration Menu Point](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ProfileColorMenu.png)
		
If you have chosen the **default** ColorProfile the menu point is disabled.
		
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
		 
If you press **OK** the selected features will be colored. 
If you press **Cancel** changes will be discarded.
    
If the selected feature already has a color, it will be shown in the dialog.
 
![ColoredFeature](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ColoredFeature.png)
		 
## 3. Results of the Coloration

Overview of the colored Views in Eclipse.
![colored views](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/coloredViews.png)
		
###3.i. Feature DiagramEditor

Colored Features in the Feature DiagramEditor.
<br>
![colored Model](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/coloredModel.png)

###3.ii. Collaboration Diagram

Colored Features in the Collaboration Diagram.
![Collaboration Diagram](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/FH_colordiagram_red_green.png)

###3.iii. FeatureIDE Outline

Colored Features in the FeatureIDE Outline.
<br>
![FeautreIDE Outline](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/FIDEOutline.png)

###3.iv. Project Explorer

A general overview how the colored Project Explorer looks.

![Project Explorer](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/FH_explorer_overview.png)

* **1**: How the Package and composed Files look in Feature House or AHEAD.

* **2**: How the Feature Folder Coloration looks in Feature House or AHEAD.

Munge and Antenna projects do not have feature folders. The Preview which kind of Feature is included in which File or Folder is only shown in the Build Folder but Munge also shows them in the source folder.

![Munge](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/ProjectExplorer_Munge.png)

###3.v. Annotations and Highlighting

Highlighting of composed files for FOP. COlors show from which module each method and fiels comes from.
![Annotations and Highlighting](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/FOP_background_code.png)

Annotations in the feature File.
![Annotations and Highlighting2](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/FeatureAnnotation.png)

###3.vi. Configuration Tree/Advanced Configuration Tree		

Colored Features in the Configuration Tree of the chosen configuration.
![Configuration Tree](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/configTree.png)

Colored Features in the Advanced Configuration Tree of the chosen configuration.
<br>
![Advanced Configuration Tree](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/Colors/advancedConfigTree.png)
		 