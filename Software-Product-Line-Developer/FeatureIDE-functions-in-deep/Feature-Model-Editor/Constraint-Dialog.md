<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < **...** < [**FeatureIDE Functions in Deep**](https://github.com/FeatureIDE/FeatureIDE/wiki/FeatureIDE-Functions-in-Deep) < [**Feature Model Editor**](https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Model-Editor)

<!-- Introduction -->
Sometimes it is required to express more complex constraints inside a feature model than e.g. "feature *A* requires parent feature". However, to formulate such constraints you can use the *ConstraintDialog* which is a text-editor with auto-completion supported, auto-validity checks and other tools. 

<!-- Outline -->
1. [Overview] (#1-overview)
	1. [Create New Constraints] (#1i-create-new-constraints)
	2. [Create New Constraints Starting with Selection] (#1ii-create-new-constraints-starting-with-selection)
	3. [Editing of Existing Constraints](#1iii-editing-of-existing-constraints)
	4. [Remove Existing Constraints](#1iv-remove-existing-constraints)
	5. [Saving changes](#1v-saving-changes)
2. [More in Detail](#2-more-in-detail)
	1. [Elements of the dialog](#2-elements-of-the-dialog)
		1. [The status information panel] (#2ia-the-status-information-panel)
		2. [A list of available features and a filtering method for this list] (#2ib-a-list-of-available-features-and-a-filtering-method-for-this-list)
		3. [The list of available operators (and, or, ...)] (2ic-#the-list-of-available-operators-and-or-)
		4. [A free-text editor where you can formulate constraints according to the grammar] (#2id-a-free-text-editor-where-you-can-formulate-constraints-according-to-the-grammar)
		5. [The dialog's control buttons] (#2ie-the-dialogs-control-buttons)
	2. [About different States to Leaving the Dialog] (#2ii-about-different-states-to-leaving-the-dialog)
	3. [Creating Constraints with or without the keyboard] (#2iii-creating-constraints-with-or-without-the-keyboard)
	4. [Constraint Free Style Text Input and it's Grammar] (#2iv-constraint-free-style-text-input-and-its-grammar)
		1. [The Need and Use of Quotes] (#2iva-the-need-and-use-of-quotes)
	5. [Live-Checks On Your Constraint](#2v-live-checks-on-your-constraint)

<!-- Content -->
## 1. Overview

### 1.i. Create New Constraints
To open the *ConstraintDialog*, right-click on a feature name inside a feature model and select *"Create Constraint"* in the popup menu. This will open the ConstraintDialog with an empty input textfield. 

![Create Constraint](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/ConstraintDialog/CreateConstraintNoRef.png)

### 1.ii. Create New Constraints Starting with Selection
If you want to start directly with your selected feature *A* you can alternativaletly click von *"Create Constraint start with *A*"* in the popup menu. This will copy *A* to the textfield which means you can immeditaly start to model the constraint related to *A*. 

![Create Constraint from Feature Name](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/ConstraintDialog/CreateConstraint.png)

### 1.iii. Editing of Existing Constraints
You can edit a constraint inside a feature model by right-clicking on it, followed by the corresponding popup menu entry.

![Edit existing Constraint](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/ConstraintDialog/EditConstraint.png)

### 1.iv. Remove Existing Constraints
By hitting *DEL* on your keyboard you can remove a selected constraint from your model. Alternatively, you can also use the popup menu by right-clicking on the constraint you want to remove.

### 1.v. Saving changes
When you finished your work, you can save you constraint to your model. Afterwards your constraint will be displayed below your feature model view where you can edit or remove it by right-clicking on it.

## 2. More in Detail

### 2.i. Elements of the dialog
The dialog contains of five regions, from up to down: 

#### 2.i.a. The status information panel
This panel contains a short info about the current dialog's state. This could be either creating or editing a constraint. Moreover it displays information, warnings or and details if an error occurs.

![Info Panel](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/ConstraintDialog/InfoPanel.png)

#### 2.i.b. A list of available features and a filtering method for this list 
Here you can click on to automatically copy-paste your selected feature into the free-text editor (see list item 4) at the current caret position. 

![Feature List](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/ConstraintDialog/FeatureList.png)

#### 2.i.c. The list of available operators (and, or, ...)
Here you can click on to automatically copy-paste a operator into the free-text editor (see list item 4).

![Operator List](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/ConstraintDialog/OperatorList.png)

#### 2.i.d. A free-text editor where you can formulate constraints according to the grammar
This control is the central element inside the *ConstraintDialog*. Here you can formulate your constraint as a first-order-logic like text, containing feature names and operators. Please note the grammar below.

![TextField](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/ConstraintDialog/ConstraintDialogText.png)

#### 2.i.e. The dialog's control buttons
Where you can save or abort your constraint. 

### 2.ii. About different States to Leaving the Dialog
Please note, that depending on the complexity of your model some constraint/feature model checks could be delayed and not finished when you want to save your constraint. In this case the dialog presents a **Save (Unchecked)** OK-Button and a short description inside the info-area (see list item 1, above). However, as long as your constraint matches the grammar, you can store/update it. Only if your constraint contains syntax error, you won't be able to store it.

### 2.iii. Creating Constraints with or without the keyboard
The *ConstraintDialog* is designed to be used with both - mouse or keyboard. You can completely edit your constraint by using the feature list and operator list without hitting any key on your keyboard. Alternatively you can input you constraint as text directly. In this case an automatic **Content Proposal Popup** will assist you while writing. This proposal opens either after 500ms or immediately by pressing *Ctrl+Space* shortcut. It contains the list of features and operators and supports auto-completion.

### 2.iv. Constraint Free Style Text Input and it's Grammar	
A constraint is built of features, operators and braces, e.g. 

```FeatureA and not(FeatureB implies not (FeatureC or (FeatureD iff FeatureE)))```

The editor supports you with syntax-highlighting for keywords. Those keywords are:

* **Operators**: (and, or, not, implies, iff) and
* **Braces**: ( and )

An incomplete constraint will also be underlined. If the syntax of the constraint is considered wrong, then the whole constraint will be underlined. Otherwise, only the specific part of the constraint which has issues or inconsistencies will be underlined.

#### 2.iv.a. The Need and Use of Quotes
If a feature to insert contains *white spaces* or conflicts to on **keywords** above, it has to be surrounded with quotes, e.g. 

```("My Feature" implies Operators) and (Operators implies ("or" or "and"))``` 

where *My Feature* contains white spaces and the user feature *Operators* requires two other feature which names are exactly like the operators in the constraint grammar. However, both the list of features and the content proposal assist you with this handling. If you select a feature where quotes are needed both controls will automatically insert them.

### 2.v. Live-Checks On Your Constraint	
Depending on your model, your input will have some affects to the model which may not be wanted or may not be obvious. One can image a constraint to exclude some features when a specific one is selected. But this could lead to a feature inside the feature model that could never be selected anymore (*Dead feature*). As the feature modeler assist you with those analysis, the ConstraintEditor does it too while you are writing you constraint. Here, the following checks are executed on your model (those checks *assume* that you will save your constraint and check how this influences the model):

1. Is your constraint a tautology?
2. Is the model satisfiable at all with you constraint?
3. Does your constraint voids the model?
4. Does your constraint produce features which are not optional although they should be?
5. Does it lead to features which are not selectable in any case?
6. Is your constraint redundant?

These checks are executed in asynchronous way to prevent blocking the user interface when applying them to huge models. For those models there is a state where some of those checks are not completed when you want to save your constraint. You can store your constraint *any way* and don't have to wait until each check passes. 

However, please note that there is also a syntax check. If your constraint does not pass the syntax check, it cannot be saved. 