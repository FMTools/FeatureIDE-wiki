<!-- Breadcrumb -->
[**HOME**](https://github.com/tthuem/FeatureIDE/wiki) < ... < [**Testing Process**](https://github.com/tthuem/FeatureIDE/wiki/Testing-Process) < [**Additional manual testing**](https://github.com/tthuem/FeatureIDE/wiki/Additional-manual-testing)

<!-- Introduction --> 
under construction

<!-- Outline -->

<!-- Content -->
# Feature Diagram
## Connections and properties
## Create/Edit/Delete diagram elements
## Drag and drop
## Legend/Highlighting
# Constraint editor
To check if the entire functionality of the *ConstraintDialog* is available after changes in code, you have to ensure that the following does not fail on at least on **Microsoft Windows** and the last official supported **JDK** version:

# Unit tests
For some core functionalities there are *JUnit tests* which should pass after your changes. These tests are

in `/de.ovgu.featureide.fm.ui-test/src/de/ovgu/featureide/fm/ui/editors/`

* `de.ovgu.featureide.fm.ui.editors.ConstraintContentProposalProviderTest`  which tests the content of the the proposal for different contexts, e.g. showing *not* only if this operator is possible to a given text and caret position. **Please note**: Currently there are some tests disabled because the filtering functionality was removed. When this functionality is available again, please enable these tests and make sure that they pass.

* `de.ovgu.featureide.fm.ui.editors.ContentProposalActionTest` which tests how the text inside the text control changes if a proposal action is accepted. *Example*: Assume that two pipes mark a selection and one pipe the caret position, then the acceptation of an item `C` in the proposal for a text `A and |B|` should change this text to `A and C|`.

# Functionality tests on the UI

The following text describe functionality which should available after your changes:

### Closing the Dialog
* Hitting *ESC* should close the dialog if no proposal is open. This should be the same as *Cancel* Button click
* Hitting *ESC* when the proposal is open should close the proposal not the dialog
* The button OK should only be disabled if the text contains syntax errors or the text control is empty

### Dialog in general
* Resizing the dialog should more or less place the controls in a accessible way, e.g. using Layouts
* For new constraints: The info panel at the top should display something like *Create new constraint*
* For editing constraints: The info panel at the top should display something like *Editing constraint*
* Below the bold printed info label, there is a description field with scroll bars. Please make sure that large text is accessible in a user friendly way

### Central controls
* Ensure that the feature filter text control works, which means that it filters the list of features according to the input
* Ensure that the feature list displays all model's feature and adds them correctly to the text field. Try feature names like *"   "*, *"  a  "* and *"or"* as well as *" or "*
* Ensure that a click of the operators-button insert the text correctly
* Ensure that the syntax highlighting works. That mean that 
    * all operators and *(* and *)* should be highlighted. 
    * Unknown feature names should be underlined. 
    * If the text contains syntax errors the entire text should be underlined.
* The proposal for the text field should open around 500ms after waiting or immediately after pressing *Ctrl+Space* at the keyboard

### More details to the ConstraintDialog as "BlackBox"
* The bold info label at the top should be decorated with
    * An *error mark* icon for syntax errors
    * An *exclamation mark* icon if at least one of the tests (tautology,...) fails
* For each test in
    * Is your cosntraint a tautology?
    * Is the model satisfiable at all with you constraint?
    * Does your constraint voids the model?
    * Does your constraint produce features which are not optional although they should be?
    * Does it lead to features which are not selectable in any case?
    * Is your constraint redundant?   
  which are automatically startet when changing the text inside constraint text field, ensure that they finish in
    * a reasonable time depending on the model size
    * That all tests are actually executed
    * All tests (expect the syntax check) are run in a sequence parallel to the UI thread. Ensure that for a given failing test the tail of this sequence is not executed.
    * Ensure that syntax problems disable the dialogs OK-Button and prevent the dialog from starting the parallel checks task
    * Ensure that the parallel test task is canceled when the user changes the text field text.
    * they could fail and deliver a good explanation about what's wrong
    * they could pass if nothing go wrong
    * That during the test phase, the user is informed about this progress (currently there is a *Save (Unchecked)* Button text for the OK-Button as well as a short description in the details text in top of the dialog)
    * If the dialog is non-modal, ensure that changes in the model are accepted. Otherwise the problem of synchronization between the model and the dialog should not be a problem because of the modularity of the dialog.

There was also a lot of work in issue [210](https://github.com/tthuem/FeatureIDE/issues/210) which should be covered with the Unit-Tests above. However, maybe it is worth to have a look on this issue to ensure that the result is still achievable.
   
# Feature order
# Propagation of changes/ View synchronization
# Feature model edits
# Outline view