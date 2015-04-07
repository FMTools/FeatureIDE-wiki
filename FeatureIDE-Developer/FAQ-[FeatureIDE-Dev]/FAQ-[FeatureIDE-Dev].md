Why are the symbols in cross-tree constraints below the feature diagram are not displayed correctly?

Please make sure that the font "Arial Unicode MS" is installed on your operating system so that FeatureIDE can use it to display the cross-tree constraints.
How can I use external jar files in my FeatureIDE project?

For FeatureIDE 2.4 and older: Please create a folder named "lib" at the project root and insert all jar files which you intent to reference. The jar files are detected by the compiler and added as parameters if you run your FeatureIDE application. 
For FeatureIDE 2.5 and newer: Right click the jar files in package explorer and add them to the Java build path.
How can I compare two different feature models in FeatureIDE?

Prepare two FeatureIDE projects (A and B) that contain the feature models you want to compare. Either edit them using FeatureIDE or import them from other formats, e.g., GUIDSL.
Open the feature model of project A, switch to the tab Source, and copy the whole document.
Open the feature model of project B, switch to the tab Source, and paste the clipboard.
Switch back to the tab Feature Diagram in editor of project B and the feature model edit view will show the results.
Checkout this video to see how to do it.
How can I import/export the feature model from/to other tools?

Select the file model.xml in Package Explorer and open the context menu > FeatureIDE > Import/Export ...
How can I store my feature model to a bitmap graphic or PDF file?

Select or open your feature model and then choose "File" > "Save As" or "File" > "Print". The later option requires that you have an PDF printer installed and have a program to crop PDFs (such as Adobe Acrobat). 
Note, that you can change the layout of the feature model since FeatureIDE 2.6 using "Set Layout" in the context menu of the feature model editor. There are pre-defined layouts, but you can also manually move features for compact positioning.