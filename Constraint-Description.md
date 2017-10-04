# Constraint Description
# 2. More in Detail
## 2.i. Elements of the dialog

The dialog contains of five regions, from up to down:
### 2.i.a. The status information panel
![Info panel](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/ConstraintDialog/InfoPanel.png)

This panel contains a short info about the current dialog's state. This could be either creating or editing a constraint. Moreover it displays information, warnings or and details if an error occurs.

### 2.i.b. A list of available features and a filtering method for this list
![Feature List](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/ConstraintDialog/FeatureList.png)

Here you can click on to automatically copy-paste your selected feature into the free-text editor (see list item 4) at the current caret position.

### 2.i.c. A text box to insert the description for this constraint
![Constraint Description Field](https://user-images.githubusercontent.com/32126942/31176517-6542b0d4-a913-11e7-8144-857821f40bd0.png)

Here you can add and edit a description.

### 2.i.d. The list of available operators (and, or, ...)
Here you can click on to automatically copy-paste a operator into the free-text editor (see list item 4).

![Operator List](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/ConstraintDialog/OperatorList.png)

### 2.i.e. A free-text editor where you can formulate constraints according to the grammar
![TextField](https://raw.githubusercontent.com/wiki/FeatureIDE/FeatureIDE/Assets/ConstraintDialog/ConstraintDialogText.png)
This control is the central element inside the ConstraintDialog. Here you can formulate your constraint as a first-order-logic like text, containing feature names and operators. Please note the grammar below.

### 2.i.f. The dialog's control buttons

Where you can save or abort your constraint.
## 2.ii. About different States to Leaving the Dialog

Please note, that depending on the complexity of your model some constraint/feature model checks could be delayed and not finished when you want to save your constraint. In this case the dialog presents a **Save (Unchecked)** OK-Button and a short description inside the info-area (see list item 1, above). However, as long as your constraint matches the grammar, you can store/update it. Only if your constraint contains syntax error, you won't be able to store it.
## 2.iii. Creating Constraints with or without the keyboard

The ConstraintDialog is designed to be used with both - mouse or keyboard. You can completely edit your constraint by using the feature list and operator list without hitting any key on your keyboard. Alternatively you can input you constraint as text directly. In this case an automatic **Content Proposal Popup** will assist you while writing. This proposal opens either after 500ms or immediately by pressing _Ctrl+Space_ shortcut. It contains the list of features and operators and supports auto-completion.

## 2.iv. Constraint Free Style Text Input and it's Grammar

A constraint is built of features, operators and braces, e.g.

FeatureA and not(FeatureB implies not (FeatureC or (FeatureD iff FeatureE)))

The editor supports you with syntax-highlighting for keywords. Those keywords are:
* **Operators**: (and, or, not, implies, iff) and
* **Braces**: ( and )

### 2.iv.a. The Need and Use of Quotes

If a feature to insert contains _white spaces_ or conflicts to on **keywords** above, it has to be surrounded with quotes, e.g.

`("My Feature" implies Operators) and (Operators implies ("or" or "and"))`

where _My Feature_ contains white spaces and the user feature _Operators_ requires two other feature which names are exactly like the operators in the constraint grammar. However, both the list of features and the content proposal assist you with this handling. If you select a feature where quotes are needed both controls will automatically insert them.

## 2.v. Live-Checks On Your Constraint

Depending on your model, your input will have some affects to the model which may not be wanted or may not be obvious. One can image a constraint to exclude some features when a specific one is selected. But this could lead to a feature inside the feature model that could never be selected anymore _(Dead feature)_. As the feature modeler assist you with those analysis, the ConstraintEditor does it too while you are writing you constraint. Here, the following checks are executed on your model (those checks _assume_ that you will save your constraint and check how this influences the model):

1. Is your constraint a tautology?
1. Is the model satisfiable at all with you constraint?
1. Does your constraint voids the model?
1. Does your constraint produce features which are not optional although they should be?
1. Does it lead to features which are not selectable in any case?
1. Is your constraint redundant?

These checks are executed in asynchronous way to prevent blocking the user interface when applying them to huge models. For those models there is a state where some of those checks are not completed when you want to save your constraint. You can store your constraint _any way_ and don't have to wait until each check passes.

However, please note that there is also a syntax check. If your constraint does not pass the syntax check, it cannot be saved.

`You may also visit FeatureIDE's home page: https://featureide.github.io/`
