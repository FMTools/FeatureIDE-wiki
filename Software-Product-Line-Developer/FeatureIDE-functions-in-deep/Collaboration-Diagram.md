# Collaboration Diagram
The **collaboration view** gives a detailed overview on the implementation of the product line, such as classes, features, and methods similar to the known Eclipse outline view, however for the whole product line. Features are displayed as columns. The attached classes are displayed as rows. If a class contains a implementation of a feature (e.g., a feature module of a processor annotation), a role is displayed as box at the intersection of the class and the feature.
The order of features is equivalent to the order defined in the feature model. Thus, if relevant for the composition tool, roles are introduced at the top and refined by roles below. 

The collaboration view can be filtered for fields, methods, refinements, contracts, invariants, nested classes, and access-modifiers. You can select multiple rows, columns or fields. Methods and classes with refinements are displayed bold (i.e., methods that are refined in several features). New roles can be created and deleted within the collaboration diagram. If you hover over a role it shows a tooltip with informations about the number of fields, methods and nested classes per role. In the top right you have buttons in a toolbar.

The function of the **toolbar** from left to right: 

![Collaboration-view_toolbar](http://i.imgur.com/uRXr0ez.jpg)
* access-modifiers-filter: filter for "private","public","protected" and "default" modifiers
* fields-with-refinements-filter: toggles the display of fields with refinements
* fields-without-refinements-filter: toggles the display of fields without refinements
* methods-with-refinements-filter: toggles the display of methods with refinements
* methods-without-refinements-filter: toggles the display of methods without refinements
* contract-filter: if enabled shows only methods with contracts
* invariant-filter: if enabled shows fields/methods with invariants
* nested-class-filter: if enabled shows nested classes
* export all: export collaboration view as image/.xml
* refresh: refresh the collaboration view

## nested-classes-toggle:

nested-classes-button **OFF** (nested classes **are not** displayed):

[![nestedclasses_off](http://i.imgur.com/yKoFjewm.jpg)](http://i.imgur.com/yKoFjew.jpg) 

nested-classes-button **ON** (nested classes **are** displayed):

[![nestedclasses_on](http://i.imgur.com/xKIsKnIm.jpg)](http://i.imgur.com/xKIsKnI.jpg) 


## Filtered for methods with refinements:

methods-with-refinements-filter **OFF** (Only methods without refinements are displayed):                    
    
[![methods_refinements_off](http://i.imgur.com/EJLJ9bwm.jpg)](http://i.imgur.com/EJLJ9bw.jpg) 

methods-with-refinements-filter **ON** (All methods are displayed):    
 
[![Methods_refinements_on](http://i.imgur.com/kHdFgd7m.jpg)](http://i.imgur.com/kHdFgd7.jpg) 

##**Example project:**

[![example](http://i.imgur.com/fWFuEJDl.png)](http://i.imgur.com/fWFuEJD.png)