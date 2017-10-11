<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < **...** < [**FeatureIDE Functions in Deep**](https://github.com/FeatureIDE/FeatureIDE/wiki/FeatureIDE-Functions-in-Deep) < [**Feature Model Editor**](https://github.com/FeatureIDE/FeatureIDE/wiki/Feature-Model-Editor)

<!-- Introduction -->
## Introduction
This section describes the feature diagram of FeatureIDE

<!-- Outline -->
## Outline
1. [Feature Diagram] (#1-feature-diagram)  
    1. [Feature Types] (#1i-feature-types)  
        1. [Concrete Feature] (#1ia-concrete-feature)  
        2. [Abstract Feature] (#1ib-abstract-feature)  
        3. [Concrete Hidden Feature] (#1ic-concrete-hidden-feature)  
        4. [Indeterminate Hidden Feature] (#1id-indeterminate-hidden-feature)  
    2. [Connection Types] (#1ii-connection-types)  
        1. [Mandatory Feature] (#1iia-mandatory-feature)  
        2. [Optional Feature] (#1iib-optional-feature)  
        3. [And] (#1iic-and)  
        4. [Or] (#1iid-or)  
        5. [Alternative] (#1iie-alternative)  
    3. [Other Types] (#1iii-other-types)  
        1. [Dead Feature] (#1iiia-dead-feature)  
        2. [False-Optional Feature] (#1iiib-false-optional-feature)  
        3. [Collapsed Feature] (#1iiic-collapsed-feature)
        4. [Redundant Constraint] (#1iiid-redundant-constraint)


***

<!-- Content -->
## 1. Feature Diagram
<p align="center">
<img alt="Feature Diagram Example" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/FeatureDiagram.png">
</p>
The feature diagram is the graphical representation of the feature model.
It shows not only the features, the feature attributes and dependencies, but also the overall constraints.
The legend provides information about the used elements in the feature diagram.

### 1.i. Feature Types:

#### 1.i.a. Concrete Feature:
<img width="105px" align="left" alt="Concrete Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Concrete.png">

A feature that will be implemented.

#### 1.i.b. Abstract Feature:
<img width="105px" align="left" alt="Abstract Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Abstract.png">

A feature used to build groups of features with a specific connection (e.g. [And] (#1iic-and)). It will not be implemented.

#### 1.i.c. Concrete Hidden Feature:
<img width="105px" align="left" alt="Concrete Hidden Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/ConcreteHidden.png">

This feature will not be shown in configurations.

#### 1.i.d. Indeterminate Hidden Feature:
<img width="105px" align="left" alt="Indeterminate Hidden Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/IndeterminateHidden.png">
This feature will not be shown in configurations.

### 1.ii. Connection Types:

#### 1.ii.a. Mandatory Feature:
<img width="32px" align="left" alt="Mandatory Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Mandatory.png">

This feature must be chosen in all configurations.

#### 1.ii.b. Optional Feature:
<img width="32px" align="left" alt="Optional Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Optional.png">

This feature can be chosen in all configurations.

#### 1.ii.c. And:
<img width="32px" align="left" alt="And" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/And.png">

All features under this connection can be chosen as optional or mandatory.

#### 1.ii.d. Or:

<img width="32px" align="left" alt="Or" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Or.png">

At least one or more features under this connection must be chosen.

#### 1.ii.e. Alternative:

<img width="32px" align="left" alt="Alternative" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/Alternative.png">

Exactly one feature under this connection must be chosen.

### 1.iii. Other Types:

#### 1.iii.a. Dead Feature:

<img width="64px" align="left" alt="Dead Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/DeadFeature.png">

A warning that a feature exists which cannot be chosen in any valid configuration.  
This feature can theoretically be removed. Check your Constraints.  

#### 1.iii.b. False-optional Feature:

<img width="64px" align="left" alt="False-Optional Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/FalseOptionalFeature.png">

A warning that a feature exists which is marked as optional, but is always required.  
This feature can theoretically be mandatory. Check your Constraints.  

#### 1.iii.c. Collapsed Feature (NEW in Version 3.3):

<img width="64px" align="left" alt="Collapsed Feature" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/under_construction.png">

A feature is collapsed and has 'n' children.  
See more information under FeatureModelEditorCollapse  

#### 1.iii.d. Redundant Constraint:

<img width="64px" align="left" alt="Redundant Constraint" src="https://github.com/FeatureIDE/FeatureIDE/wiki/Assets/FeatureModelEditor/FeatureDiagram/RedundantConstraint.png">

A warning that a redundant constraint exists.
This constraint can theoretically be removed.  

