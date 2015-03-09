To check if the entire functionality of the *ConstraintDialog* is available after changes in code, you have to ensure that the following does not fail:

# Unit tests
For some core functionalities there are *JUnit tests* which should pass after your changes. These tests are

in `/de.ovgu.featureide.fm.ui-test/src/de/ovgu/featureide/fm/ui/editors/`

* `de.ovgu.featureide.fm.ui.editors.ConstraintContentProposalProviderTest`  which tests the content of the the proposal for different contexts, e.g. showing *not* only if this operator is possible to a given text and caret position. **Please note**: Currently there are some tests disabled because the filtering functionality was removed. When this functionality is available again, please enable these tests and make sure that they pass.

* `de.ovgu.featureide.fm.ui.editors.ContentProposalActionTest` which tests how the text inside the text control changes if a proposal action is accepted. *Example*: Assume that two pipes mark a selection and one pipe the caret position, then the acceptation of an item `C` in the proposal for a text `A and |B|` should change this text to `A and C|`.

# Functionality tests on the UI