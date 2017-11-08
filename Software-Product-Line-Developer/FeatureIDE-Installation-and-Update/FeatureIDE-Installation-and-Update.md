<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < [**Software Product Line Developer**](https://github.com/FeatureIDE/FeatureIDE/wiki/Software-Product-Line-Developer)

<!-- Introduction -->
In the following, we give brief introduction how we prepare pre-packaged versions of Eclipse for our [website](https://featureide.github.io/#download). In case we have already a version for your operating system, you can use it instead of the instructions below to save time. In case you have another operating system or want to setup the Eclipse on your own, you might want to use the following instructions.

We distinguish two pre-packaged versions for FeatureIDE. If you only aim to feature model and configuration editor and you are not interested in the composition of artifacts (e.g., source code), scroll down. In case you aim to setup an Eclipse with all of FeatureIDE's functionality (including numerous composers), use the following instructions:

<!-- Outline -->

<!-- Content -->
1. Download "Eclipse for Committers" or any other version of Eclipse from https://eclipse.org/downloads/eclipse-packages/
2. Unzip eclipse into a folder where you have full permissions (e.g., under Windows it is recommended to use another folder than "program files") 
4. Start Eclipse and create a new workspace (e.g., "../workspace")
   
   It is recommended to use a folder that is not indexed by Windows as this may cause weird interactions with git.
5. Install required plug-ins:
   - Install [CDT](https://eclipse.org/cdt/downloads.php) (required if you are working C or C++, or if you want to compile the FeatureIDE extension Colligens, which is recommended) <img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/Installation/cdt.png">
   - Install [AJDT](https://eclipse.org/ajdt/downloads/) (only required if you are working with AspectJ) <img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/Installation/ajdt.png">
   - Install [FeatureIDE](http://featureide.cs.ovgu.de/update/v3/) <img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/Installation/featureide-allplugins.png">
   - Restart eclipse after installation of new plug-ins 
6. Open the FeatureIDE perspective

If you only aim to feature model and configuration editor and you are not interested in the composition of artifacts (e.g., source code):

1. Download "Eclipse Platform Runtime Binary" from https://download.eclipse.org/eclipse/downloads/
2. Unzip eclipse into a folder where you have full permissions (e.g., under Windows it is recommended to use another folder than "program files") 
4. Start Eclipse and create a new workspace (e.g., "../workspace")
   
   It is recommended to use a folder that is not indexed by Windows as this may cause weird interactions with git.
5. Install required plug-ins:
   - Install [FeatureIDE](http://featureide.cs.ovgu.de/update/v3/) <img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/Installation/featureide-pure.png">
     
     Alternatively, you may also experiment with only installing feature modeling to even reduce the size of Eclipse. However, many nice features of FeatureIDE are not available then. <img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/Installation/featureide-onlyfeaturemodeling.png">
   - Restart eclipse after installation of new plug-ins 
6. Open the FeatureIDE perspective
