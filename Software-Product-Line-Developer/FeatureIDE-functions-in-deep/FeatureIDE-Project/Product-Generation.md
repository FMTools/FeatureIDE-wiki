<!-- Breadcrumb -->
[**HOME**](https://github.com/tthuem/FeatureIDE/wiki) < [**Software Product Line Developer**](https://github.com/tthuem/FeatureIDE/wiki/Software-Product-Line-Developer) < [**FeatureIDE Functions in Deep**](https://github.com/tthuem/FeatureIDE/wiki/FeatureIDE-Functions-in-Deep) < [**FeatureIDE Project**](https://github.com/tthuem/FeatureIDE/wiki/FeatureIDE-Project)

<!-- Introduction -->
A main goal of software-product-line engineering is to derive customized products from a common code base.
With FeatureIDE we automated this process.

In FeatureIDE you always have on current configuration that is generated. 
The current configuration is built from the feature folder into the source folder of the underlying project.

_You can set the current configuration with right-click on the configuration you want to generate and select _FeatureIDE > Set as current configuration__. The current configruration is marked with the green pen.

To automatically build the current configuration if there are changes in the project activate _Project > Build Automatically_.
The product is only generated if there are changes in the feature files of the selected features or the feature model has changed (i.e., the generated product would differ).

After the source files are generated, the underlying compiler automatically detects changes and thus compiles the program.

_You should not change the generated files (except if the feature files are the same as the source files) as your changes are lost after you start the build process again._

The build process of the generation tools is specialized for their approaches. We illustrate the general process as follows.

Preprocessors (Antenna, CPP) do not have a separate folder for their source files. They compile the files in the source folder directly. 

<img width="250" src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureIDEProject/Antenna.PNG">

The preprocessor Munge generates new preprocessed source files from a feature folder. 

<img width="250" alt="under_construction" src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureIDEProject/Munge.PNG">

AspectJ weaves the aspects into the class files. Aspects that are not selected are not in the build path, and thus are not includes in the generated product.

<img width="250" alt="under_construction" src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureIDEProject/AspectJ.PNG">

Feature-oriented composition tools (FeatureHouse, AHEAD, FeatureC++) have one feature module (i.e. folder) for each concrete feature.
The selected feature modules are composed by the composition tool into the source folder. 

<img width="250" alt="under_construction" src="https://github.com/tthuem/FeatureIDE/wiki/Assets/FeatureIDEProject/FH.PNG">
