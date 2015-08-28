<!-- Breadcrumb -->
[**HOME**](https://github.com/tthuem/FeatureIDE/wiki) < [**Software Product Line Developer**](https://github.com/tthuem/FeatureIDE/wiki/Software-Product-Line-Developer) < [**FeatureIDE Functions in Deep**](https://github.com/tthuem/FeatureIDE/wiki/FeatureIDE-Functions-in-Deep)

<!-- Introduction -->

<!-- Outline -->

<!-- Content -->
The configuration editor helps to customize you program. The editor is always in sync with the feature model of the FeatureIDE project. For example, if you rename a feature in the model, also the feature in configuration file is renamed, too. 
Furthermore, the configuration editor checks whether the configuration is valid to the feature model. The validity of the configuration is shown in the header of the editor. Furthermore, the number of configurations that can have the configuration as partial configuration is shown in the header, too.

_You can open a configuration with the configuration editor with a double-click on a configuration file._

The **default page** shows the configuration as tree similar to the structure defined in the feature model.
Selected features are either marked with an check mark or with a box. The box indicated that the selection of the feature is implied by other feature selections; such features cannot be deselected manually until the other feature is deselected. The check mark indicates that the feature is selected manually, thus the features can also be deselected manually. A gray coloring indicates that the feature cannot be selected anymore because of the selection of other features. 

_If the selection of a feature is implied (i.e., the feature must be selected or deselected) by other features, FeatureIDE automatically sets the selection of these features._

<img width="300" 
src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureModelEditor/ConfigurationEditor/configuration.PNG">

The configuration editor gives some help to guide you to a valid configuration. If the selection or deselection of one feature can make a configuration valid, this feature is highlighted with green if it needs to be selected of blue if it needs to be deselected.

<img width="300" src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureModelEditor/ConfigurationEditor/configurationhelp.PNG">

The configuration editor has several pages. You can select other pages at the bottom of the editor.
The "**Advanced Configuration**" page provides some additional functionality to the first page. 
Here you can additionally mark features to be deselected by right-clicking the feature. You can also see the connection type of the features (e.g., whether it is a mandatory feature). 

<img width="300" src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureModelEditor/ConfigurationEditor/advancedpage.PNG">

The "**source page**" shows the content of the file. You can use this page to copy other configuration. After you go back to one of the configuration pages the editor features are automatically selected.

We recommend not to use the source view to editor the configuration, as you do not have assists such as checks whether the feature exists or the configuration is valid.

<img width="300" 
src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureModelEditor/ConfigurationEditor/sourcepage.PNG">


[coloration](https://github.com/tthuem/FeatureIDE/wiki/Coloration)is supported.