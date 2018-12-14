<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < [**Software Product Line Developer**](https://github.com/FeatureIDE/FeatureIDE/wiki/Software-Product-Line-Developer) < [**Background**](https://github.com/FeatureIDE/FeatureIDE/wiki/Background)

<!-- Introduction -->

<!-- Feature States -->

The Layout is seperated into two different files (.xml and .xml.xml).

   * .xml:
   The .xml file stores the feature model. This includes constraints and feature information like name, abstract, mandatory, description and their heritage.

   * .xml.xml:
   You can find the .xml.xml file in the hidden folder .featureide/model.xml of the project. It contains information about the layout of the model, the selected layouting algorithm, information about the layouting algorithm, and which features are collapsed. If the manual layout algorithm is selected, the position of each feature is saved here.
If the .xml.xml file does not already exist when opening a feature model in FeatureIDE, the file is created, and the model size is adjusted to the editor size (class FeatureModelEditor). 