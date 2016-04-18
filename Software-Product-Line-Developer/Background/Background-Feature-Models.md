<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < [**Software Product Line Developer**](https://github.com/FeatureIDE/FeatureIDE/wiki/Software-Product-Line-Developer) < [**Background**](https://github.com/FeatureIDE/FeatureIDE/wiki/Background)

<!-- Introduction -->
under construction

<!-- Feature States -->

| **State**   	| **Description**  	|
|---	|---	|
| Alternative group | Exactly one of the features in this group must be selected, if the parent feature is selected.  	|
| Or Group | At least one of the features in this group must be selected, if the parent feature is selected. |
| Optional feature | This feature does not have to be selected. |
| Mandatory feature | This feature must be selected whenever its parent is selected. |
| Abstract feature | This feature does not has any impact at implementation level. |
| Imported feature | This feature is imported from another feature model. |
| Inherited feature | This feature is inherited from a parent feature model. |
| Interface feature | This feature is a feature from an interface. |
| Concrete feature | This feature has impact at implementation level. |
| Hidden feature | This feature will not be shown in the configuration editor. Non-hidden features should determine when to select the feature automatically |
| Dead feature | This feature cannot be selected in any valid configuration. |
| False optional feature | This feature is declared optional, but is always selected if the parent feature is selected. |
| Indeterminate hidden feature | This feature is declared hidden, but does not depend on any unhidden features. |
| Redundant constraint | This constraint does not change the product line. |
| Unsatisfiable Constraint | This constraint cannot become true |
| Constraint is tautology | This constraint cannot become false. |
| Constraint makes the model void. | Constraint makes the model void. |

