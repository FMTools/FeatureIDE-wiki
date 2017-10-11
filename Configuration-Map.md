<!-- Breadcrumb -->
// [**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < [**Software Product Line Developer**](https://github.com/FeatureIDE/FeatureIDE/wiki/Software-Product-Line-Developer) < [**FeatureIDE Functions in Deep**](https://github.com/FeatureIDE/FeatureIDE/wiki/FeatureIDE-Functions-in-Deep)

<!-- Introduction -->
 
_**This part has already been updated for version 3.3.**_
 
The Configuration Map shows a table of which features are used in which configuration.
There are severeal filter options to allow a comparative view between configurations.

<!-- Outline -->
1. [General View] (#1-general-view)
2. [Filter Options](#2-filter-options)
3. [Opening Configuration Files] (#3-opening-configuration-files)
4. [Colors] (#4-colors)


<!-- Content -->
## 1. General View
 
The Configuration Map shows all configurations of a project which features are selected in them. 
The features can be folded and expanded like a tree structure. When the Map is opened, it’s fully expanded.
 
![Configuration Map](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/ConfigurationMap/ConfigurationMap.png)
 
![aselected](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/ConfigurationMap/aselected.ico)
Indicates, if a feature is selected in this configuration.
 
![adeselected](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/ConfigurationMap/adeselected.ico)
Indicates, if a feature is disabled in this configuration.
 
## 2. Filter Options
 
Different filters are supported, so you can choose some to have a better view at the existing configurations.
These filters are disjunct to each other, thereby are many different possibilities to filter.
 
![Configuration Map Filters](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/ConfigurationMap/ConfigurationMapFilters.png)
 
* **Core features**: If enabled, it shows all features, which have to be selected in every configuration.
* **False-optional features**: If enabled, it shows all features, which are selected in every configuration but are actually optional features.
* **Unused features**: If enabled, it shows all features, which are disabled in every configuration.
* **Dead features**: If enabled, it shows all features, which can’t be selected in any configuration.
* **Remaining features**: If enabled, it shows all features, which aren’t contained in the other filters.

 
## 3. Opening Configuration Files
 
To open a configuration file from the ConfigMap, you can doubleclick its header or use the context menu. It will be opened in the editor.
 
## 4. Colors
 
[Colors](https://github.com/FeatureIDE/FeatureIDE/wiki/Colors) are supported.