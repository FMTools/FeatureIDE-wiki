Plugins

* de.ovgu.featureide.core - common functionality of FeatureIDE: nature, builders, marker, common model
* de.ovgu.featureide.core.ahead - composition plugin for AHEAD: mixin wrapper, parsing from AST, specific model(?), error markers
* de.ovgu.featureide.core.ahead.refactoring - plugin that provides refactoring options for jak code. Requires AHEAD.
* de.ovgu.featureide.core.featurecpp - composition plugin for FeatureC++: call to command line tool, TODO structure parsing from special output
* de.ovgu.featureide.core.featurehouse - composition plugin for FeatureHouse: fh wrapper, parsing from FST
* de.ovgu.featureide.ui - common UI: buttons, decorators, new project wizard, ...
* de.ovgu.featureide.ui.ahead - Jak wizard, Jak editor with syntax highlighting and outline view
* de.ovgu.featureide.ui.doc - Sheat cheets explaining the usage, ...
* de.ovgu.featureide.fm.core - feature model core: parsing and writing, reasoning, configurations
* de.ovgu.featureide.fm.core-test - JUnit tests
* de.ovgu.featureide.fm.ui - feature model UI: graphical feature model editor, configuration/equation editor, import/export

Other:

* plugins/de.ovgu.featureide.* - a folder containing all FeatureIDE plugins
* lib/Ahead - extension of AHEAD that is included as jar in the FeatureIDE_Core plugin
* lib/TypeSystem - type system extension of AHEAD that is included as jar in the FeatureIDE_Refactoring plugin
* deploy/UpdateSite - deployment only
* deploy/de.ovgu.featureide - the main eclipse feature containing almost all FeatureIDE plugins
* deploy/de.ovgu.featureide.featurecpp - the eclipse feature containing the FeatureC++ plugin
* deploy/de.ovgu.featureide.featurehouse - the eclipse feature containing the FeatureHouse plugin
* projects/* - example FeatureIDE projects including implementation
* featuremodels/* - example FeatureIDE projects, feature model without code
* doc/* - documentation, slides, papers