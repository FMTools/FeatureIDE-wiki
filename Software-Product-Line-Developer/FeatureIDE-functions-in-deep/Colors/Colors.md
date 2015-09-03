<!-- Breadcrumb -->
[**HOME**](https://github.com/tthuem/FeatureIDE/wiki) < [**Software Product Line Developer**](https://github.com/tthuem/FeatureIDE/wiki/Software-Product-Line-Developer) < [**FeatureIDE Functions in Deep**](https://github.com/tthuem/FeatureIDE/wiki/FeatureIDE-Functions-in-Deep)

<!-- Introduction -->

An example of how to colorate a featureHouse project.

<!-- Outline -->
1. [How to manipulate ColorProfiles] (#1-how-to-manipulate-colorprofiles)
	1. [Create New ColorProfile] (#1i-create-new-colorprofile)
	2. [Rename ColorProfile] (#1ii-rename-colorprofile)
	3. [Delete ColorProfile](#1iii-delete-colorprofile)
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
## 1. How to manipulate ColorProfiles

### 1.i. Create new ColorProfile
Rightclick on a Featureproject to get into the FeatureIDE menu. To be able to color a feature you need to add a new Profile because the **default** Profile is not able to apply colors and is therefore used for statistics and calculations.
		
![Create new ColorProfile](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/DynamicMenuStructure.png)
		
Click Add Colorscheme to add a new Colorscheme.
		
![Create new Colorscheme Wizard](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/AddProfile.png)
		
### 1.ii. Rename ColorProfile

Open the FeatureIDE menu as shown above. If you click on Change Name you can rename your Profile.
		
![Rename Colorscheme Wizard](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/RenameProfile.png)
		
### 1.iii. Delete ColorProfile

Open the FeatureIDE menu as shown above. If you click on Delete Colorscheme you will delete your Profile and the active profile will be set to **default**.
		
## 2. Coloration
		
### 2.i. Coloration Menu Point

Rightlick on FeatureDiagramm to open the ContextMenu and use the menu point as shown below.
		
![Coloration Menu Point](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/ProfileColorMenu.png)
		
If you have chosen the **default** ColorProfile the menu point is disabled.
		
### 2.ii. Coloration Dialog

If the menu point is not disabled you will open a Coloration Dialog. 

![Empty Color Dialog](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/EmptyColorDialog.png)
		 
The Coloration Dialog offers two important options. 
		 
* **Action**: As shown below you can choose one of those actions. 
		 
![action DropDownDialog](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/actionDropDownDialog.png)
		  
* **Color**: You can choose one of ten baseline colors.
		 
![color DropDownDialog](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/colorDropDownDialog.png)
		 
In the preview you see the visualization of the colored features.
		 
![color PreviewDialog](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/colorPreviewDialog.png)
		 
If you press okay the coloration of the selected features will be made.
If you press cancel changes will be discarded.
		 
## 3. Results of the Coloration

Overview of the colored Views in Eclipse.
![colored views](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/coloredViews.png)
		
###3.i. Feature DiagramEditor

Colored Features in the Feature DiagramEditor.
<br>
![colored Model](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/coloredModel.png)

###3.ii. Collaboration Diagram

Colored Features in the Collaboration Diagram.
![Collaboration Diagram](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/FH_colordiagram_red_green.png)

###3.iii. FeatureIDE Outline

Colored Features in the FeatureIDE Outline.
<br>
![FeautreIDE Outline](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/FIDEOutline.png)

###3.iv. Project Explorer

A general overview how the colored Project Explorer looks.

![Project Explorer](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/FH_explorer_overview.png)

* **1**: How the Package and composed Files look in Feature House or AHEAD.

* **2**: How the Feature Folder Coloration looks in Feature House or AHEAD.

Munge and Antenna projects do not have feature folders. The Preview which kind of Feature is included in which File or Folder is only shown in the Build Folder but Munge also shows them in the source folder.

![Munge](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/ProjectExplorer_Munge.png)

###3.v. Annotations and Highlighting

Highlighting of composed files for FOP. COlors show from which module each method and fiels comes from.
![Annotations and Highlighting](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/FOP_background_code.png)

Annotations in the feature File.
![Annotations and Highlighting2](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/FOP_background_code_red.png)

###3.vi. Configuration Tree/Advanced Configuration Tree		

Colored Features in the Configuration Tree of the chosen configuration.
![Configuration Tree](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/configTree.png)

Colored Features in the Advanced Configuration Tree of the chosen configuration.
<br>
![Advanced Configuration Tree](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Colors/advancedConfigTree.png)
		 