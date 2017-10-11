<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < ... < [**Getting started**](https://github.com/FeatureIDE/FeatureIDE/wiki/Getting-started) < [**Preparing Eclipse**](https://github.com/FeatureIDE/FeatureIDE/wiki/Preparing-Eclipse)

<!-- Introduction -->

<!-- Outline -->

<!-- Content -->
### 1. Line Endings and Encoding
  * Go to **Window -> Preferences**.
  * Open page **General -> Workspace**.
    * Set _text file encoding_ to **UTF-8**.
    * Set _new text file line delimiters_ to **Unix**.

* If you already have files in your workspace with Non-Unix line endings, do the following:
  * Select all projects in the navigator or package explorer view (you can also only select the single files).
  * In the menu click on **File -> Convert Line Delimiters To -> Unix**.

### 2. Source Code Formatter
  * Go to **Window -> Preferences**.
  * Open page **Java -> Code Style -> Formatter**.
     * Click on _Import..._ and open the file `Conventions.xml` in the `de.ovgu.featureide.fm.core` plug-in