1. Download Eclipse from https://eclipse.org/downloads/
- Unzip Eclipse into a folder where you have full permissions (it is recommended not to use the "program files" folder) 
- Create shortcut to start eclipse with the folowing VM options:
 
   \- vmargs -Xmx1g -XX:MaxPermSize=256M (only required for Java 7 and lower)
   
   Avoids out of memory errors
- Start Eclipse and create a new workspace
   
   It is recommended to use a folder that is not indexed by Windows as this may cause interactions with git
- Install required plug-ins _Help > Install new Software..._ or _Help > Eclipse Marketplace..._:
 1. Install [CDT](https://eclipse.org/cdt/downloads.php) (only required if you are working C or C++)
 - Install [AJDT](https://eclipse.org/ajdt/downloads/) (only required if you are working with AspectJ)
 - Restart eclipse after installation of new plug-ins 
- Install FeatureIDE via Eclipse marketplace or with our [update site](http://wwwiti.cs.uni-magdeburg.de/iti_db/research/featureide/deploy/) (_you may also use our [nightly build](http://wwwiti.cs.uni-magdeburg.de/iti_db/research/featureide/nightly/p2-updateSite/)_)
 - Select all plugins you need:
    - The plug-in "Feature Modelling" is required for modeling
     - The plug-in "FeatureIDE" is required for software product line development
     - The plug-in "FetureIDE example projects" contains several examples you may want to check out
     - The other plug-ins are specialized composition tools
