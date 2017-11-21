<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < **...** < [**FeatureIDE Functions in Deep**](https://github.com/FeatureIDE/FeatureIDE/wiki/FeatureIDE-Functions-in-Deep) < [**Feature Model Editor**](https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Model-Editor)


# Introduction

This section describes the Feature Order View of FeatureIDE.

<!-- Outline -->
# Outline
1. [Feature Order View]
    1. [Using the Feature Order View]
    2. [Updating the position of features]
        1. [Buttons]
        2. [Drag and Drop]


***

<!-- Content -->
# Feature Order View
<p align="center">
<img alt="Feature Diagram Example" src="https://github.com/Henningson/FeatureIDETeam2/wiki/Assets/FeatureModelEditor/FeatureOrder/FeatureOrderViewBase.png">
</p>

The Feature Order View is a tool to sort the features to determine in which order the features should get compiled.

Remember that using the Feature Order View is only possible by using a FeatureIDE Project that is not for modelling purposes only.
In short, creating, for example, an Antenna, FeatureHouse or Munge Project will enable the Feature Order View.

## Using the Feature Order View
To use the Feature Order View select the tab "Feature Order" at the bottom of the Feature Model View.

<p align="center">
<img alt="Feature Order Select1" src="https://github.com/Henningson/FeatureIDETeam2/wiki/Assets/FeatureModelEditor/FeatureOrder/FeatureOrderSelect1.png">
</p>

Then just select the checkbox "User-defined feature order".

<p align="center">
<img alt="Feature Order Select2" src="https://github.com/Henningson/FeatureIDETeam2/wiki/Assets/FeatureModelEditor/FeatureOrder/FeatureOrderSelect2.png">
</p>

## Updating the position of features
To update the position of features using the Feature Order View, just select the features you want to move. Then you can choose between the following two possibilites to order the features.

To simplify matters, changing the order of the features in the Feature Model Diagram will also update the position of the features in the Feature Order View and vice versa.

### Buttons

**Up:** The Up-Button moves the selected features one column up.

**Down:** The Down-Button moves the selected features one column down.

**Default:** The Default-Button sorts the features by using a pre-order traversal method.
You can find more about pre-order traversal [here].

### Drag and Drop
You can also position features by using Drag and Drop.
Select the features you want to position, hold left-click and position your mouse at the column at which you want to insert them.

[here]: https://en.wikipedia.org/wiki/Tree_traversal#Pre-order
[Feature Order View]: https://github.com/Henningson/FeatureIDETeam2/wiki/Feature-Order#feature-order-view
[Using the Feature Order View]: https://github.com/Henningson/FeatureIDETeam2/wiki/Feature-Order#using-the-feature-order-view
[Updating the position of features]: https://github.com/Henningson/FeatureIDETeam2/wiki/Feature-Order#updating-the-position-of-features
[Buttons]: https://github.com/Henningson/FeatureIDETeam2/wiki/Feature-Order#buttons
[Drag and Drop]: https://github.com/Henningson/FeatureIDETeam2/wiki/Feature-Order#drag-and-drop
