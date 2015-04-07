1. Download Eclipse from https://eclipse.org/downloads/
- Unzip eclipse into a folder where you have full permissions (it is recommended not to use the "program files" folder) 
- Create shortcut to start eclipse with the folowing VM options:
 
   \- vmargs -Xmx1g -XX:MaxPermSize=256M (only required for Java 7 and lower)
   
   Avoids out of memory errors
- Start Eclipse and create a new workspace
   
   It is recommended to use a folder that is not indexed by Windows as this may cause interactions with git
- Install required plug-ins:
 1. Install [CDT](https://eclipse.org/cdt/downloads.php) (only required if you are working C or C++)
 - Install [AJDT](https://eclipse.org/ajdt/downloads/) (only required if you are working with AspectJ)
 - Restart eclipse after installation of new plug-ins 

For installation details you might have a look in this [presentation](http://wwwiti.cs.uni-magdeburg.de/iti_db/research/featureide/slides/featureide-2-getstarted.pdf). 
