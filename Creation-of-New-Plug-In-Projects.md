This page shows the basic steps for creating a new FeatureIDE plug-in project
* Create a new Plug-In Project in your workspace via Eclipse's context menu  
General name prefix for plug-in names and packages is
_de.ovgu.featureide.core_ for core plug-ins and _de.ovgu.featureide.ui_ for UI plug-ins

* Add plug-in ID, version, and name to META-INF/MANIFEST.MF

* Add activator class to META-INF/MANIFEST.MF  
This class should extend `AbstractCorePlugin` or `AbstractUIPlugin`

* Copy license.txt from FMCorePlugin

* Create .options file  
`<plug-in name>/debug=true`  
_(replace \<plug-in name\> with the name of your plug-in)_

* Share your project in git

* Create .gitignore file  
`/bin`