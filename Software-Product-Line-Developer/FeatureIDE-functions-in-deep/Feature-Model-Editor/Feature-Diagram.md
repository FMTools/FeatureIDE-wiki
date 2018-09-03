<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < **...** < [**FeatureIDE Functions in Deep**](https://github.com/FeatureIDE/FeatureIDE/wiki/FeatureIDE-Functions-in-Deep) < [**Feature Model Editor**](https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Model-Editor)

<!-- Introduction -->
# Introduction
This section describes the feature diagram of FeatureIDE

<!-- Outline -->
# Outline
1. [Feature Diagram]
    1. [Feature Types]
        1. [Concrete Feature] 
        2. [Abstract Feature]
        3. [Concrete Hidden Feature]  
        4. [Indeterminate Hidden Feature]
    2. [Connection Types]
        1. [Mandatory Feature] 
        2. [Optional Feature] 
        3. [And]
        4. [Or]
        5. [Alternative]  
    3. [Other Types]
        1. [Dead Feature]
        2. [False-Optional Feature]
        3. [Collapsed Feature]
        4. [Redundant Constraint]
2. [Feature Diagram Layouts]
	1. [Layout-Algorithms for the Feature Order]
		1. [Manual Layout]
		2. [Top-Down (ordered)]
		3. [Top-Down (centered)]
		4. [Top-Down (left-aligned)] 
		5. [Left-To-Right (ordered)] 
	2. [Legend Auto-Layout]
	3. [Constraints Auto-Layout] 
		1. [Constraints Vertical]
		2. [Constraints Horizontal]
3. [Export]
	1. [LaTeX Export using TikZ]

***

<!-- Content -->
# Feature Diagram

<p align="center">
<img alt="Feature Diagram Example" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/FeatureDiagram.png">
</p>
The feature diagram is the graphical representation of the feature model.
It shows not only the features, the feature attributes and dependencies, but also the overall constraints.
The legend provides information about the used elements in the feature diagram.

## Feature Types:

### Concrete Feature:
<img width="105px" align="left" alt="Concrete Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Concrete.png">

A feature that will be implemented.

### Abstract Feature:
<img width="105px" align="left" alt="Abstract Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Abstract.png">

A feature used to build groups of features with a specific connection (e.g. [And]). It will not be implemented.

### Concrete Hidden Feature:
<img width="105px" align="left" alt="Concrete Hidden Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/ConcreteHidden.png">

This feature will not be shown in configurations.

### Indeterminate Hidden Feature:
<img width="105px" align="left" alt="Indeterminate Hidden Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/IndeterminateHidden.png">
This feature will not be shown in configurations.


## Connection Types:

### Mandatory Feature:
<img width="32px" align="left" alt="Mandatory Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Mandatory.png">

This feature must be chosen in all configurations.

### Optional Feature:
<img width="32px" align="left" alt="Optional Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Optional.png">

This feature can be chosen in all configurations.

### And:
<img width="32px" align="left" alt="And" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/And.png">

All features under this connection can be chosen as optional or mandatory.

### Or:

<img width="32px" align="left" alt="Or" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Or.png">

At least one or more features under this connection must be chosen.

### Alternative:

<img width="32px" align="left" alt="Alternative" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Alternative.png">

Exactly one feature under this connection must be chosen.

## Other Types:

### Dead Feature:

<img width="64px" align="left" alt="Dead Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/DeadFeature.png">

A warning that a feature exists which cannot be chosen in any valid configuration.  
This feature can theoretically be removed. Check your Constraints.  

### False-optional Feature:

<img width="64px" align="left" alt="False-Optional Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/FalseOptionalFeature.png">

A warning that a feature exists which is marked as optional, but is always required.  
This feature can theoretically be mandatory. Check your Constraints.  

### Collapsed Feature:

<img width="64px" align="left" alt="Collapsed Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/CollapsedFeature.png">

A feature is collapsed and has 'n' children.  
See more information under FeatureModelEditorCollapse  

### Redundant Constraint:

<img width="64px" align="left" alt="Redundant Constraint" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/RedundantConstraint.png">

A warning that a redundant constraint exists.
This constraint can theoretically be removed.  

# Feature Diagram Layouts:

## Layout-Algorithms for the Feature Order

There are currently four different kinds of layout-algorithms usable in FeatureIDE, aswell as one option for manually adjusting the Feature Layout. These can be selected by right-clicking and selecting the wanted layout at "Set Layout" in the Feature Diagram Editor.

The following paragraphs will show you the different kinds of aforementioned algorithms currently available in FeatureIDE.

### Manual Layout

<img alt="Manual Layout" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Layout/Manual.png">

### Top-Down (ordered)

<img alt="Top-Down (ordered)" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Layout/TopDownOrdered.png">

### Top-Down (centered)

<img alt="Top-Down (centered)" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Layout/TopDownCentered.png">

### Top-Down (left-aligned)

<img alt="Top-Down (left-aligned)" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Layout/TopDownLeftAligned.png">

### Left-To-Right (ordered)

<img alt="Left-To-Right (ordered)" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Layout/LeftToRightOrdered.png">

## Abego Layouts
The following layouts are examples using abego TreeLayout library. They are defined by the root position at the top, bottom, left and right side.  The new added layouts are with the root positions at the bottom and right side.  
### Root Top (abego TreeLayout)
If the root is at the top the tree will grow from top to the bottom. It works like Top-Down(ordered).
<img alt="Root Top (abego TreeLayout)" src="https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/FeatureModelEditor/FeatureDiagram/Layout/RootTopAbego.png">
### Root Left (abego TreeLayout)
If the root is at the left side, tree will grow from right to left. It works like Left-to-Right(ordered).
<img alt="Root Left (abego TreeLayout)" src="https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/FeatureModelEditor/FeatureDiagram/Layout/RootLeftAbego.png">
### Root Right (abego TreeLayout)
If the root is at the right side, the tree will grow from right to left.
<img alt="Root Right (abego TreeLayout)" src="https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/FeatureModelEditor/FeatureDiagram/Layout/RootRightAbego.png">
### Root Bottom (abego TreeLayout)
If the root is at the bottom, the tree will grow from the bottom up to the top.
<img alt="Root Bottom (abego TreeLayout)" src="https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/FeatureModelEditor/FeatureDiagram/Layout/RootBottomAbego.png">


## Legend Auto-Layout

If the legend is visible, you can right-click on it to open its context menu. Selecting "Auto-Layout Legend" will activate a mode in which the legend will try to fit itself in one of the four positions (1 to 4) shown in the image below. If there is no empty space left, it will be placed next to the Feature Diagram (5).

<p align="center">
<img alt="Layout Legend Algorithm" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Layout/LayoutLegendAlgorithm.png">
</p>

## Constraints Auto-Layout

Unless not specifically selected, FeatureIDE will automatically position the constraints depending on the position of the root element and on the layout-algorithm selected. Two examples are given below.

### Vertical Layout Example
<p align="center">
<img alt="Auto-Layout Constraints Vertical" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Layout/AutoLayoutConstraintsVertical.png">
</p>

### Horizontal Layout Example
<p align="center">
<img alt="Auto-Layout Constraints Horizontal" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Layout/AutoLayoutConstraintsHorizontal.png">
</p>

# Export
You can export your feature diagram in many formats, e.g. *.png, *.jpg, *.bmp and *.tex.
For this, make sure nothing is selected and then click with your secondary mouse button in free space of your feature model editor to open the context menu. Then click "Export As". It opens a dialog where you can name it and choose in which format you want to save your file.

## LaTeX Export using TikZ
If you want to use a feature diagram in your LaTeX document, you can simply choose to export your diagram as *.tex file. This generate a new folder with the name you given in which you find three different LaTeX files:
* **head.tex** In this file you will find the required styles and packages for your Feature Diagram.
* **your_file_name.tex** This is the main file. Therefore it is named as your given name (in the dialog where you want to save your file). Here you will find the exported Feature Diagram. You can simply integrate this file in your own document with the command `\include{your_file_name.tex}`. Make sure that you integrate the required styles and packages for this file in your own document too, which you can find in "head.tex", so that the feature model can be displayed correctly.
* **body.tex** This file only brings the other files together to easily compile the code.  

<p align="center">
<img alt="body.tex" src="">
</p>


By using the LaTeX Exporter, there are at the moment some restrictions:
* You can only export the layout _Top-Down (centered)_.
* Customized Colors will be not exported.
* Hidden features are not supported and will be shown as normal features.
* Dead and false-optional features, as well as redundant constraints will be not declared as such.


[Feature Diagram]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#feature-diagram
[Feature Types]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#feature-types
[Concrete Feature]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#concrete-feature
[Abstract Feature]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#abstract-feature
[Concrete Hidden Feature]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#concrete-hidden-feature
[Indeterminate Hidden Feature]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#indeterminate-hidden-feature
[Connection Types]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#connection-types
[Mandatory Feature]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#mandatory-feature
[Optional Feature]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#optional-feature 
[And]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#and
[Or]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#or
[Alternative]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#alternative 
[Other Types]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#other-types
[Dead Feature]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#dead-feature
[False-Optional Feature]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#false-optional-feature
[Collapsed Feature]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#collapsed-feature
[Redundant Constraint]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#redundant-constraint
[Feature Diagram Layouts]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#feature-diagram-layouts
[Layout-Algorithms for the Feature Order]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#layout-algorithms-for-the-feature-order
[Manual Layout]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#manual-layout
[Top-Down (ordered)]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#top-down-ordered
[Top-Down (centered)]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#top-down-centered
[Top-Down (left-aligned)]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#top-down-left-aligned
[Left-To-Right (ordered)]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#left-to-right-ordered
[Legend Auto-Layout]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#legend-auto-layout
[Constraints Auto-Layout]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#constraints-auto-layout
[Constraints Vertical]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#vertical-layout-example
[Constraints Horizontal]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#horizontal-layout-example
[Export]: https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#export
[LaTeX Export using TikZ]:https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Diagram#latex-export-using-tikz