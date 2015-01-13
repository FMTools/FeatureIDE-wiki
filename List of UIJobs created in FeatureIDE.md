This table gives an overview of all classes extending UIJob. They might affect the responsiveness of the UI if they are nonperformant, high load, or scheduled with too high priority.

<table width= 100%>
    <tr>
        <td>Title</td>
        <td>Job type</td>
        <td>Instantiating class</td>
        <td>Description</td>
    </tr>
    <tr>
        <td>Refresh statistics view</td>
        <td>UIJob</td>
		<td>de.ovgu.featureide.ui.statistics.ui.helper.JobDoneListener</td>
		<td>Displays feedback on Jobs scheduled by an IJobChangeEvent. Instantiated once to show the feedback and once to remove it.</td> 
    </tr>
	<tr>
        <td>resort node</td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.ui.statistics.ui.helper.TreeClickListener)</td>
        <td>Refreshes the TreeViewer.</td>
    </tr>
	<tr>
        <td>Updating feature model attributes</td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.fm.ui.editors.FeatureDiagramEditor</td>
        <td>Sets feature status and constraint attribute to "NORMAL" and refreshes the Viewers contents.</td>
    </tr>
	<tr>
        <td>Update Collaboration View</td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.ui.views.collaboration.CollaborationView</td>
        <td>Sets viewer contents and refreshes them; Enables the toolbarAction and refreshes the search content.</td>
    </tr>
	<tr>
        <td></td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.ui.statistics.core.CsvExporter</td>
        <td>Displays the Dialog for the CSVExport. Its JobChangeListeners done() method starts the export for a non null return value.</td>
    </tr>
	<tr>
        <td>"show errordialog" or "show dialog"</td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.ui.statistics.core.CsvExporter</td>
        <td>Opens a MessageDialog that reports the successful export being done, if it was successful. Otherwise the MessageDialog reports, that the file could not be accessed and prompts, if it should try again.</td>
    </tr>
	<tr>
        <td>init dialog - treeviewer</td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.ui.statistics.ui.CheckBoxTreeViewDialog</td>
        <td>Sets the viewers content and refreshes it.</td>
    </tr>	
	<tr>
        <td></td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.featurecpp.wrapper.FeatureCppWrapper</td>
        <td>Displays a MessageBox if FeatureC++ could not be executed because of insufficient permissions. It is instantiated in the deprecated private method openMessageBox.  </td>
    </tr>	
	<tr>
        <td>Creating Android project</td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.ui.wizards.NewFeatureProjectWizard</td>
        <td>Creates an android project by calling the wizardExtensions performBeforeFinish() method.</td>
	</tr>
	<tr>
        <td>refresh tree</td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.fm.ui.editors.configuration.AdvancedConfigurationPage</td>
        <td></td>
	</tr>
	<tr>
        <td>refresh source page</td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.fm.ui.editors.configuration.ConfigurationEditor</td>
        <td>Refreshes the TextEditorPage by calling its propertyChange() method with null parameter.</td>
	</tr>
	<tr>
        <td>refresh tree</td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.fm.ui.editors.configuration.ConfigurationPage</td>
        <td></td>
	</tr>
	<tr>
        <td>Refresh edit view</td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.fm.ui.views.featuremodeleditview.ViewContentProvider</td>
        <td>calls the TreeViewers refresh() method, unless the TreeViewer is disposed</td>
	</tr>
	<tr>
        <td>Refresh statistics view</td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.ui.statistics.core.ContentProvider</td>
        <td>calls the TreeViewers refresh() method, unless the TreeViewer is disposed</td>
	</tr>
	<tr>
        <td>Updating feature model attributes</td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.fm.ui.editors.FeatureDiagramEditor</td>
        <td>Mind that there are two methods in the class, which create this job, although both seem to do the same. One is created by the StoppableJob "Analyze feature model", the other one by the private method refreshGraphics()</td>
	</tr>
	<tr>
        <td>Refresh export dialog</td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.ui.statistics.ui.CheckBoxListener</td>
        <td>calls the CheckboxTreeViewers refresh() method</td>
	</tr>
	<tr>
        <td></td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.fm.ui.editors.configuration.ConfigurationPage</td>
        <td>Sets color and font of a TreeItem</td>
	</tr>
	<tr>
        <td>Converting Feature Models</td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.fm.ui.views.FeatureModelEditView</td>
        <td>calls method convertModelToBitmapTest(..)</td>
	</tr>
	<tr>
        <td>Update Outline View</td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.ui.views.collaboration.outline.Outline</td>
        <td>sets and updates various fields of the TreeViewer depending on its status</td>
	</tr>
	<tr>
        <td>Save image</td>
        <td>UIJob</td>
        <td>de.ovgu.featureide.fm.ui.editors.featuremodel.GEFImageWriter</td>
        <td>Saves the GEF editors content in a bitmap by calling saveEditorContentsAsImage(..)</td>
	</tr>
</table>