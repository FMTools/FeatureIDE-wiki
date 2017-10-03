<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < [**FeatureIDE Developer**](https://github.com/FeatureIDE/FeatureIDE/wiki/FeatureIDE-Developer) < [**Development Process in general**](https://github.com/FeatureIDE/FeatureIDE/wiki/Development-Process-in-general) < [**Testing-Process-overview**](https://github.com/FeatureIDE/FeatureIDE/wiki/Testing-Process-overview)

# Introduction
This section is about setting up and running FeatureIDE GUI-Tests. FeatureIDE GUI-Tests are used to test features where interaction with the GUI is necessary.

# Outline
1. Setup Eclipse
2. Setup RCPTT Project

# Content

## 1. Setup Eclipse

1. Download [Eclipse Neon RCP](http://www.eclipse.org/downloads/packages/eclipse-rcp-and-rap-developers/neon3).
2. Open Eclipse -> Help -> Eclipse Marketplace -> Search for ```RCPTT``` and Install ```RCPTT - Eclipse UI Testing Tool```.
3. (optional, for c++ user) Open Eclipse -> Help -> Eclipse Marketplace -> Search for ```CDT``` and Install ```Eclipse C/C++ IDE CDT 9.2```.
4. Import all FeatureIDE projects into the workspace.

## 2. Setup RCPTT Project

### Create RCPTT Project
Now you need to create a project that holds all files for your tests. We will be creating a test for the feature model editor that is part of the ```de.ovgu.featureide.fm.ui``` plugin. Therefore our RCPTT project will be named ```de.ovgu.featureide.fm.ui-gui-test```.

1. Open the RCPTT perspective.
2. Right-Click test explorer -> New -> RCP Testing Tool Project.
3. Set your desired project name and hit Finish.

### Register Application Under Test
We now need to create a new AUT. The AUT is the eclipse instance where you record and perform the GUI-Tests. Follow the steps to register your AUT:

1. In the View Applications at the button of the screen right-click -> New...
2. Click Browse...
3. Explorer dialog appears now select the folder of your eclipse installation. 
4. The name should be automatically resolved. Now click Finish.

### Deploy FeatureIDE plugins to your AUT
For your tests to test FeatureIDE feature your AUT needs to have FeatureIDE installed.

1. Click File -> Export -> Deployable plug-ins and fragments -> Next.
2. Select all Plugins.
3. Select the plugin folder of your AUT as Directory in Destination. For example: ```C:\Users\Hans\Desktop\eclipse\plugins```.
4. Click Options and check ```Package plug-ins as individual JAR archives```.
5. Click Finish.

You can now test if everything is setup correctly by running your AUT and looking for the FeatureIDE perspective and views.

### Create Contexts
To perform our tests we need to create some contexts and verification. Contexts are used to tell the test for example which project is available, which perspective should be active at runtime. Verifications are the requirements that should verify if the test is successful or not. 

We want our feature model editor tests to have the FeatureIDE perspective to be open when starting the test. We also want the example project ```Elevator-FeatureModeling-Colored``` to be imported.

A. Context ```FeatureIDE perspective```
1. In ```Test Explorer``` right-click your project -> New -> Context
2. Type in the name ```FeatureIDE Workbench```
3. As type for the context select ```Workbench```
4. You can now select every view or editor that should be active when starting the test. The easiest way is to click Capture.
5. Now Select your AUT and click OK.
6. Your AUT will now start. (When an error appears to try again)
7. Switch to your AUT and click Window -> Perspective -> FeatureIDE Perspective
8. Switch to your first eclipse instance and click Capture again.

B. Context ```FeatureModel - Colored Workspace```
1. On your project right-click -> New -> Context.
2. Select as type ```Workspace``` and type name ```FeatureModel - Colored Workspace```.
3. Click Finish.
4. Open context and click ```Import Projects...````
5. Select as root directory ```%FEATURE_IDE_PATH%\plugins\de.ovgu.featureide.examples\featureide_examples\Book\FM\Elevator-FeatureModeling-Colored```
6. Now select the Project ```Elevator-FeatureModeling-Colored``` and click Finish.

Close the AUT and run the AUT again.

### Create Verifications
Now when we start the test we take the source of the feature model and do our operation. After the operations, we take the source again and test if they are equal.

1. Project -> right-click -> New -> Verification.
2. Set Name ```Feature Model Source```.
3. Select Widget Text and click Finish.
4. Open Verification and click Capture.
5. Open model.xml from the ```Elevator-FeatureModeling-Colored``` project. Switch to the source tab and click on the source. It should now automatically switch back to your first instance of eclipse.

## Create Test

1. Right-click project -> New -> Test Case.
2. Type Name ```AddFeatures```.
3. Click Record.
4. Open model.xml.
5. Add features. (multiple times)
6. Save feature model. (CTRL+S)
7. Redo all actions. (CTRL+Z)
8. Save again.
9. Switch to the script COntrol Panel and click Stop.
10. Contexts -> Add -> FeatureIDE Workbench
11. Contexts -> Add -> FeatureModel - Colored Workspace
12. Verifications -> Add -> Feature Model Source

Test is now created and ready.

## RunTest

1. Right-click on AddFeatures -> Run As -> Test Case


