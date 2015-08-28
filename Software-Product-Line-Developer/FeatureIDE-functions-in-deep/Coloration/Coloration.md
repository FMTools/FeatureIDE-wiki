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
4. [Different Composers](#4-different-composers)
	1. [Preprocessor (Antenna & Munge)](#4i-preprocessor-(antenna-&-munge))
	2. [FeatureHouse and AHEAD](#4ii-featurehouse-and-ahead)


<!-- Content -->
## 1. How to manipulate ColorProfiles

### 1.i. Create new ColorProfile
Rightclick on a Featureproject to get into the FeatureIDE menu. To be able to color a feature you need to add a new Profile because the **default** Profile is not able to apply colors and is therefore used for statistics and calculations.
		
![Create new ColorProfile](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/DynamicMenuStructure.png)
		
Click Add Colorscheme to add a new Colorscheme.
		
![Create new Colorscheme Wizard](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/AddProfile.png)
		
### 1.ii. Rename ColorProfile

Open the FeatureIDE menu as shown above. If you click on Change Name you can rename your Profile.
		
![Rename Colorscheme Wizard](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/RenameProfile.png)
		
### 1.iii. Delete ColorProfile

Open the FeatureIDE menu as shown above. If you click on Delete Colorscheme you will delete your Profile and the active profile will be set to **default**.
		
![Delete Colorscheme](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/DeleteProfile.png)
		
## 2. Coloration
		
### 2.i. Coloration Menu Point

Rightlick on FeatureDiagramm to open the ContextMenu and use the menu point as shown below.
		
![Coloration Menu Point](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/ProfileColorMenu.png)
		
If you have chosen the **default** ColorProfile the menu point is disabled.
		
![Default Coloration Menu Point](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/DefaultColorMenu.png)
		
### 2.ii. Coloration Dialog

If the menu point is not disabled you will open a Coloration Dialog. 

![Empty Color Dialog](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/EmptyColorDialog.png)
		 
The Coloration Dialog offers two important options. 
		 
* **Action**: As shown below you can choose one of those actions. 
		 
![action DropDownDialog](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/actionDropDownDialog.png)
		  
* **Color**: You can choose one of ten baseline colors.
		 
![color DropDownDialog](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/colorDropDownDialog.png)
		 
In the preview you see the visualization of the colored features.
		 
![color PreviewDialog](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/colorPreviewDialog.png)
		 
If you press okay the coloration of the selected features will be made.
If you press cancel changes will be discarded.
		 
## 3. Results of the Coloration

![colored views](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/coloredViews.png)
		
###3.i. Feature DiagramEditor

![colored Model](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/coloredModel.png)

###3.ii. Collaboration Diagram

![Collaboration Diagram](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/FH_colordiagram_red_green.png)

###3.iii. FeatureIDE Outline

![FeautreIDE Outline](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/coloredViews.png)

###3.iv. Project Explorer

A general overview how the Project Explorer looks.

![Project Explorer](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/FH_explorer_overview.png)

How the Package and composed Files look.
<br>

![Project Explorer Package](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/FH_explorer_main_3colors.PNG)
<br>
How the Feature Folder Coloration looks in Feature House or AHEAD.
<br>
![Project Explorer Features](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/FH_explorer_features.PNG)
<br>
###3.v. Annotations and Highlighting

Annotations in the composed File including Highlighting. Highlighting can be enabled or disabled in the JavaEditor context menu.
![Annotations and Highlighting](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/FOP_background_code.png)

Annotations in the feature File.
![Annotations and Highlighting2](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/FOP_background_code_red.png)

###3.vi. Configuration Tree/Advanced Configuration Tree		
	
![Configuration Tree](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/configTree.png)

Advanced Configuration
<br>
![Advanced Configuration Tree](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/advancedConfigTree.png)

##4. Different Composers

###4.i. Preprocessor (Antenna & Munge)

These projects do not have feature folders. The Preview of what kind of Feature is included in which File or Folder is only shown in the Build Folder but Munge also shows them in the source folder.

![Munge](https://raw.githubusercontent.com/wiki/tthuem/FeatureIDE/Assets/Coloration/ProjectExplorer_Munge.png)

###4.ii. FeatureHouse and AHEAD

FeatureHouse and AHEAD both have feature folders. The previous Screenshot in 3.iv. of our Project Explorer applies for AHEAD.
		
		
		 