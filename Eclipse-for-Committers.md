<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < ... < [**Getting started**](https://github.com/FeatureIDE/FeatureIDE/wiki/Getting-started) < [**Preparing Eclipse**](https://github.com/FeatureIDE/FeatureIDE/wiki/Preparing-Eclipse)

<!-- Introduction -->

<!-- Outline -->

<!-- Content -->
1. Download "Eclipse for Committers" from https://eclipse.org/downloads/eclipse-packages/
2. Unzip eclipse into a folder where you have full permissions (it is recommended not to use the "program files" folder) 
3. Create shortcut to start eclipse with the folowing VM options:
 
   \- vmargs -Duser.name="Name Surename"
   
   Eclipse will automatically insert you name as author if you create a new Class

4. Start Eclipse and create a new workspace
   
   It is recommended to use a folder that is not indexed by Windows as this may cause interactions with git
5. Install required plug-ins:
   - Install [CDT](https://eclipse.org/cdt/downloads.php) (required if you are working C or C++, or if you want to compile the FeatureIDE extension Colligens, which is recommended) <img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/Installation/cdt.png">
   - Install [AJDT](https://eclipse.org/ajdt/downloads/) (only required if you are working with AspectJ) <img src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/Installation/ajdt.png">
   - Restart eclipse after installation of new plug-ins 
