The current configuration is build/composed/preprocessed from the feature folder into the source folder of the underlying project. 

You set the current configuration with right-click on the configuration you want to generate and select _FeatureIDE > Set as current configuration_

To automatically build the current configuration (marked the the green pen) you can activate _Project > Build Automatically_
The product is there are changes in the feature files of the selected features or the feature model has changed.


After the source files are generated the underlying compiler should automatically detect changes and thus should compile the program. 

You should not change the generated files (except if the feature files are the same as the source files) as your changes are lost after you start the build process again.

