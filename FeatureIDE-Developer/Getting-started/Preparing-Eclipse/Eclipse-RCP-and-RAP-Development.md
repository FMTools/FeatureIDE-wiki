1. Download "Eclipse for RCP and RAP Developers" from https://eclipse.org/downloads/
- Unzip eclipse into a folder where you have full permissions (it is recommended not to use the "program files" folder) 
- Create shortcut to start eclipse with the folowing VM options:
 
   \- vmargs -Duser.name="Name Surename" -Xmx1024M
   
   Eclipse will automatically insert you name as author if you create a new Class<br>
   Avoids out of memory errors
- Start Eclipse and create a new workspace
   
   is is recommended to use a folder that is not indexed by Windows as this may cause interactions with git
- Install required plug-ins:
 1. Install CDT (only required if you are working C or C++)
 - Install AJDT (only required if you are working with AspectJ)
 - Install a git plug-in (e.g. EGit) to manage the repository from within Eclipse (not required)
 - Restart eclipse after installation of new plug-ins 
