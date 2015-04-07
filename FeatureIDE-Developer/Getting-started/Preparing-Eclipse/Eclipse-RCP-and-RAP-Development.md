This is a detailed installation guide to setup your system for the development of FeatureIDE.

1 Download "Eclipse for RCP and RAP Developers" from https://eclipse.org/downloads/

2 Unzip eclipse into a folder where you have full permissions (it is recommended not to use the "program files" folder)

3 Create shortcut to start eclipse with the folowing VM options:
	- vmargs -Duser.name="Name Surename" -Xmx1024M
	
	Eclipse will automatically insert you name as Author if you create a new Class
	Avoids out of memory errors
	
4 Start Eclipse and create a new workspace
	- is is recommended to use a folder that is not indexed by Windows as this may cause interactions with git

5. Install required plug-ins:
5.1 Install CDT (only required if you are working C or C++)
5.2 Install AJDT (only required if you are working with AspectJ)
5.3 Install a git plug-ins (e.g. EGit) to manage the repository from within Eclipse (not required)
5.4 Restart eclipse after installation of new plug-ins 

