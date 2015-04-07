7. Create a new run configuration to start Eclipse with FeatureIDE plug-ins
	
	Run > Run Configurations... 
	Double click on Eclipse Application
	
7.1 Specify VM arguments at the "Arguments" page
	-Dosgi.requiredJavaVersion=1.7 -Xmx1g 
	-XX:MaxPermSize=256M (only required for Java 7 and lower)
7.2 Enable tracing at the "Tracing" page
	- select the check box "Enable tracing"
	- select all plug-ins starting with de.ovgu.featureide

7.3 run the eclipse application	
	- a second eclipse will start with all FeatureIDE plug-ins from your workspace
	
7.4 open the FeatureIDE perspective
