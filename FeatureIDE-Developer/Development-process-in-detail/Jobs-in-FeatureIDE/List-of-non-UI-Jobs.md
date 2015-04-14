<!-- Breadcrumb -->
[**HOME**](https://github.com/tthuem/FeatureIDE/wiki) < [**FeatureIDE Developer**](https://github.com/tthuem/FeatureIDE/wiki/FeatureIDE-Developer) < [**Development Process in detail**](https://github.com/tthuem/FeatureIDE/wiki/Development-Process-in-detail) < [**Jobs in FeatureIDE**](https://github.com/tthuem/FeatureIDE/wiki/Jobs-in-FeatureIDE)

<!-- Introduction -->
These Jobs extend org.eclipse.core.runtime.jobs.Job, but not org.eclipse.ui.progress.UIJob, which means they should not influence UI responsiveness. 

<!-- Outline -->


<! Content -->
<table>
    <tr>
        <td>Title</td>
        <td>Job type</td>
        <td>Instantiating class</td>
        <td>Description</td>
    </tr>
	<tr>
        <td>Enhance DeltaJ Project</td>
        <td>EnhanceProjectJob (Job)</td>
        <td>de.ovgu.featureide.deltaj.ui.wizard.DeltaJNewProjectWizardExtension</td>
        <td>Handles the work of the DeltaJNewProjectWizardExtensions createDeltas() and replaceModel() methods</td>
    </tr>
	<tr>
        <td>Checking for unused features.</td>
        <td>AWaitingJob</td>
        <td>de.ovgu.featureide.core.internal.FeatureProject</td>
        <td>Scheduled in private method checkFeatureCoverage()</td>
    </tr>
	<tr>
        <td>Synchronize feature model and feature modules</td>
        <td>AWaitingJob</td>
        <td>de.ovgu.featureide.core.internal.FeatureProject<</td>
        <td>Scheduled in private method setAllFeatureModuleMarkers()</td>
    </tr>
    <tr>
        <td>Loading Signatures for <code>projectname</code></td>
        <td>ExtendedFujiSignaturesJob (AStoppableJob)</td>
        <td>de.ovgu.featureide.featurehouse.meta.FeatureStubsGenerator</td>
        <td>Loads Signatures from fuji and calls the getFeatures(..) method on them once the Job is finished, using the JobFinishListener</td>
    </tr>
	<tr>
        <td>Type checking <code>projectname</code> with fuji</td>
        <td>AStoppableJob</td>
        <td>de.ovgu.featureide.featurehouse.FeatureHouseComposer</td>
        <td>Runs fuji then uses the results to set the SignatureSetters parameters. This is called on build and when the "use fuji" option is enabled</td>
    </tr>	
	<tr>
        <td>Calculating <code>description</code></td>
        <td>StoppableTreeJob (StoppableJob)</td>
        <td>de.ovgu.featureide.ui.statistics.core.composite.lazyimplementations.ConfigParentNode</td>
        <td>Handles work of the ConfigParentNodes public calculate(..) method, which creates a single job instance and schedules it.</td>
    </tr>
	<tr>
        <td>Refresh Collaboration View</td>
        <td>StoppableJob</td>
        <td>de.ovgu.featureide.ui.views.collaboration.CollaborationView</td>
        <td>Handles work of the toolbarActions run() method, which creates a single job instance and schedules it</td>
    </tr>	
	<tr>
        <td>Build meta product for project "<code>projectName</code>".</td>
        <td>StoppableJob</td>
        <td>de.ovgu.featureide.featurehouse.ui.actions.BuildMetaProductAction</td>
        <td>Handles work of the BuildMetaProductActions run() method, which creates a single job instance and schedules it</td>
    </tr>	
	<tr>
        <td>Analyze feature model</td>
        <td>StoppableJob</td>
        <td>de.ovgu.featureide.fm.ui.editors.FeatureDiagramEditor</td>
        <td>Is instantiated by a wrapper job to prevent the UI from freezing. Creates a UIJob (Title: "Updating feature model attributes") to update elements on the UI.</td>
    </tr>
	<tr>
        <td>Create missing configurations.</td>
        <td>StoppableJob</td>
        <td>de.ovgu.featureide.ui.quickfix.QuickFixFalseOptionalFeatures</td>
        <td>Handles work of the QuickFixFalseOptionalFeatures' run() method, which creates a single job instance and schedules it</td>
    </tr>	
	<tr>
        <td>Performing full build</td>
        <td>StoppableJob</td>
        <td>de.ovgu.featureide.core.internal.FeatureProject</td>
        <td>Calls the project builder at the end of FeatureProjects setCurrentConfiguration(..) method</td>
    </tr>
	<tr>
        <td>Loading Signatures</td>
        <td>CreateFujiSignaturesJob (AMonitorJob)</td>
        <td>de.ovgu.featureide.core.mpl.InterfaceProject</td>
        <td>Job instantiating method is called by MPLPlugin.refresh(..) and InterfaceProject.setProjectSignatures</td>
    </tr>
	<tr>
        <td>Loading Signatures</td>
        <td>CreateFujiSignaturesJob (AMonitorJob)</td>
        <td>de.ovgu.featureide.core.mpl.MPLPlugin</td>
        <td>Job instantiating method is called by 7 different methods of MPLPlugin</td>
    </tr>	
	<tr>
        <td>Generator [if more then one, appends "nr. "+index]</td>
        <td>Generator (Job)</td>
        <td>de.ovgu.featureide.ui.actions.generator.ConfigurationBuilder</td>
        <td>Instantiated and scheduled in ConfigurationBuilders createNewGenerator(..) method</td>
    </tr>
	<tr>
        <td>Compiler [if more then one, appends "nr. "+index]</td>
        <td>Compiler (Job)</td>
        <td>de.ovgu.featureide.ui.actions.generator.Compiler</td>
        <td>Compiles all configurations of the corresponding Generator</td>
    </tr>
	<tr>
        <td>Build all current configurations for <code>projectName</code></td>
        <td>Job</td>
        <td>de.ovgu.featureide.ui.actions.generator.ConfigurationBuilder</td>
        <td>Instantiated and scheduled in the ConfigurationBuilders constructor, if buildType is ALL_CURRENT</td>
    </tr>
	<tr>
        <td>Build all valid configurations for <code>projectName</code></td>
        <td>Job</td>
        <td>de.ovgu.featureide.ui.actions.generator.ConfigurationBuilder</td>
        <td>Instantiated and scheduled in the ConfigurationBuilders constructor, if buildType is ALL_VALID</td>
    </tr>
		<tr>
        <td>Build t-wise configurations for <code>projectName</code></td>
        <td>Job</td>
        <td>de.ovgu.featureide.ui.actions.generator.ConfigurationBuilder</td>
        <td>Instantiated and scheduled in the ConfigurationBuilders constructor, if buildType is T_WISE</td>
    </tr>
	<tr>
        <td>Export statistics into csv</td>
        <td>Job</td>
        <td>de.ovgu.featureide.ui.statistics.core.CsvExporter</td>
        <td>Handles the export of a TreeViewers contents to a csv file</td>
    </tr>
	<tr>
        <td>Add Project</td>
        <td>Job</td>
        <td>de.ovgu.featureide.core.CorePlugin</td>
        <td>Adds projects from the projectsToAdd field to the Plugin</td>
    </tr>
	<tr>
        <td>Calculate: "<code>statisticsText</code>"</td>
        <td>Job</td>
        <td>de.ovgu.featureide.fm.ui.views.featuremodeleditview.ViewContentProvider</td>
        <td>Calculates the number of configurations</td>
    </tr>
	<tr>
        <td>Change composer.</td>
        <td>Job</td>
        <td>de.ovgu.featureide.ahead.actions.AHEADToFeatureHouseConversion</td>
        <td>Changes project composer to FeatureHouse</td>
    </tr>
	<tr>
        <td>preprocessor annotation checking</td>
        <td>Job</td>
        <td>de.ovgu.featureide.munge.MungePreprocessor</td>
        <td>Checks the projects source folder recursively for annotations, then sets model markers</td>
    </tr>
	<tr>
        <td>Update Collaboration View</td>
        <td>Job</td>
        <td>de.ovgu.featureide.ui.views.collaboration.CollaborationView</td>
        <td>Scheduled in public method updateGuiAfterBuild(..)</td>
    </tr>
	<tr>
        <td>Calculate: "Statistics on before edit version"</td>
        <td>Job</td>
        <td>de.ovgu.featureide.fm.ui.views.featuremodeleditview.ViewContentProvider</td>
        <td>Part of the ViewContentProviders calculations in public method calculateContent(..)</td>
    </tr>
	<tr>
        <td>Call compiler</td>
        <td>Job</td>
        <td>de.ovgu.featureide.featurehouse.FeatureHouseComposer</td>
        <td>Touches the projects .classpath file to call the compiler, which is necessary after calling the method setAsCurrentConfiguration(..)</td>
    </tr>
	<tr>
        <td>Checking configurations</td>
        <td>Job</td>
        <td>de.ovgu.featureide.core.internal.FeatureProject</td>
        <td>Handles the work of FeatureProjects checkConfigurations(..) method</td>
    </tr>
	<tr>
        <td>Load Model</td>
        <td>Job</td>
        <td>de.ovgu.featureide.core.internal.FeatureProject</td>
        <td>Handles the work of FeatureProjects checkModelChange(..) method</td>
    </tr>
	<tr>
        <td>Change composer.</td>
        <td>Job</td>
        <td>de.ovgu.featureide.ahead.actions.FeatureHouseToAHEADConversion</td>
        <td>Changes a featureProjects composer to AHEAD. Instantiated and scheduled in the constructor of FeatureHouseToAHEADConversion.</td>
    </tr>
	<tr>
        <td>Propagate problem markers for <code>featureProject</code></td>
        <td>Job</td>
        <td>de.ovgu.featureide.featurecpp.wrapper.FeatureCppWrapper</td>
        <td>Handles the work of the FeatureCppWrappers private method addMarker(..). One instance of the Job is created per marker.</td>
    </tr>
	<tr>
        <td>Propagate problem markers for <code>featureProject</code></td>
        <td>Job</td>
        <td>de.ovgu.featureide.featurehouse.errorpropagation.ErrorPropagation</td>
        <td>Handles the work of the ErrorPropagations propagateMarkers(..) method. The abstract class ErrorPropagation is currently only extended by CErrorPropagation and JavaErrorPropagation</td>
    </tr>	
	<tr>
        <td>Propagate problem markers for <code>featureProject</code></td>
        <td>Job</td>
        <td>de.ovgu.featureide.ahead.wrapper.AheadWrapper</td>
        <td>Handles work of the AheadWrappers public postCompile(..) method, which creates a single job instance and schedules it.</td>
    </tr>	
	<tr>
        <td>Propagate problem markers for <code>featureProject</code></td>
        <td>Job</td>
        <td>de.ovgu.featureide.munge.MungePreprocessor</td>
        <td>Handles work of the MungePreprocessors public postCompile(..) method, which creates a single job instance and schedules it.</td>
    </tr>	
	<tr>
        <td>Analyze feature model (waiting)</td>
        <td>Job</td>
        <td>de.ovgu.featureide.fm.ui.editors.FeatureDiagramEditor</td>
        <td>Wrapper job for the Featuremodel analysis, that is necessary to prevent the UI from freezing</td>
    </tr>	
	<tr>
        <td>Updating Feature Model Edits</td>
        <td>Job</td>
        <td>de.ovgu.featureide.fm.ui.views.FeatureModelEditView</td>
        <td>Wrapper job that immediately starts a new calculation once the previous calculation job is finished. Warning: the calculation job has the exact same title.</td>
    </tr>	
	<tr>
        <td>Updating Feature Model Edits</td>
        <td>Job</td>
        <td>de.ovgu.featureide.fm.ui.views.FeatureModelEditView</td>
        <td>Handles the calculation and presentation of the FeatureModelEditors content, by calling its contentProviders calculateContent(..) method</td>
    </tr>	
	<tr>
        <td>Updating FeatureStatisticsView</td>
        <td>Job</td>
        <td>de.ovgu.featureide.ui.statistics.ui.FeatureStatisticsView</td>
        <td>Wrapper job that immediately starts a new calculation once the previous calculation job is finished. Warning: the calculation job has the exact same title.</td>
    </tr>	
	<tr>
        <td>Updating FeatureStatisticsView</td>
        <td>Job</td>
        <td>de.ovgu.featureide.ui.statistics.ui.FeatureStatisticsView</td>
        <td>Handles the calculation and presentation of the FeatureStatisticsViews content, by calling its contentProviders calculateContent(..) method</td>
    </tr>	
	<tr>
        <td>Remove project</td>
        <td>Job</td>
        <td>de.ovgu.featureide.core.internal.ProjectChangeListener</td>
        <td>Handles work of the ProjectChangeListeners private removeProject(..) method, which creates a single job instance and schedules it</td>
    </tr>	
	<tr>
        <td></td>
        <td>Job</td>
        <td>de.ovgu.featureide.fm.ui.views.FeatureModelEditView</td>
        <td>Handles work of the FeatureModelEditView.activatorActions  run() method, which creates a single job instance and schedules it</td>
    </tr>		
	<tr>
        <td>Updating Feature Model Edits</td>
        <td>Job</td>
        <td>de.ovgu.featureide.fm.ui.views.FeatureModelEditView</td>
        <td>Handles work of the FeatureModelEditView.manualActions run() method, which creates a single job instance and schedules it</td>
    </tr>	
	<tr>
        <td>Export to CNF</td>
        <td>Job</td>
        <td>de.ovgu.featureide.fm.ui.actions.ExportCNFAction</td>
        <td>Handles work of the ExportCNFActions run() method, which creates a single job instance and schedules it</td>
    </tr>		
	<tr>
        <td>Export to DIMACS</td>
        <td>Job</td>
        <td>de.ovgu.featureide.fm.ui.actions.ExportDIMACSAction</td>
        <td>Handles work of the ExportDIMACSActions run() method, which creates a single job instance and schedules it</td>
    </tr>	
	<tr>
        <td>Calculating Feature Dependencies</td>
        <td>Job</td>
		<td>de.ovgu.featureide.fm.ui.actions.FeatureDependenciesAction</td>
        <td>Handles work of the FeatureDependenciesActions run() method, which creates a single job instance and schedules it</td>
    </tr>	
	<tr>
        <td>Typechecking <code>projectName</code></td>
        <td>Job</td>
        <td>de.ovgu.featureide.core.typecheck.TypeCheckerFIDE</td>
        <td>Handles work of the TypeCheckerFIDEs run() method, which creates a single job instance and schedules it</td>
    </tr>
	<tr>
        <td>Feature coloring.(<code>fileName</code>)</td>
        <td>Job</td>
        <td>de.ovgu.featureide.fm.ui.editors.configuration.ConfigurationPage</td>
        <td>Handles work of the ConfigurationPages setColor(..) method, which creates a single job instance and schedules it</td>
    </tr>	
	<tr>
        <td>Evaluation Test</td>
        <td>Job</td>
        <td>de.ovgu.featureide.fm.ui.views.FeatureModelEditView</td>
        <td>Handles work of the Evaluation.evaluate(..) method. The setFeatureModelEditor(..) method creates a single job instance and schedules it</td>
    </tr>	
	<tr>
        <td>Create missing configurations.</td>
        <td>Job</td>
        <td>de.ovgu.featureide.ui.quickfix.QuickFixMissingFeatures</td>
        <td>Handles work of the QuickFixMissingFeatures' run() method, which creates a single job instance and schedules it</td>
    </tr>
</table>