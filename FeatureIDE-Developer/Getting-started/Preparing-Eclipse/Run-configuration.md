<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < ... < [**Getting started**](https://github.com/FeatureIDE/FeatureIDE/wiki/Getting-started) < [**Preparing Eclipse**](https://github.com/FeatureIDE/FeatureIDE/wiki/Preparing-Eclipse)

<!-- Introduction -->

<!-- Outline -->

<!-- Content -->
1. Create a new run configuration to start Eclipse with FeatureIDE plug-ins

   1. Run > Run Configurations... 
   - Double click on Eclipse Application
- Specify VM arguments at the "Arguments" page:

   -Dosgi.requiredJavaVersion=1.7<br>
   -Xmx1g<br>
   -XX:MaxPermSize=256M (only required for Java 7 and lower)
- Enable tracing at the "Tracing" page

   1. select the check box "Enable tracing"
   - select all plug-ins starting with de.ovgu.featureide
- run the eclipse application	
   a second eclipse will start with all FeatureIDE plug-ins from your workspace
- open the FeatureIDE perspective
