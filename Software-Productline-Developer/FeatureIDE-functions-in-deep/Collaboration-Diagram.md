# Collaboration Diagram
The **collaboration view** shows a table of all classes and features. Features are displayed in columns and the attached classes are displayed in rows. The collaboration view can filter for fields, methods, refinements, contracts, invariants, nested classes and access-modifiers; also you can select multiple rows, columns or fields and filter for similarities. A field in the table shows fields, methods and nested classes ordered by classes. Methods and classes with refinements have bold letters. New roles can be created and deleted within the collaboration diagram. If you hover over a role it shows a tooltip with informations about the number of fields , methods and nested classes per role. In the top right you have buttons in a toolbar to filter equal to the context menu. 

The function of the **toolbar** from left to right are: 

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


nested-classes-button **OFF** :  

[![nestedclasses_off](http://i.imgur.com/yKoFjewm.jpg)](http://i.imgur.com/yKoFjew.jpg) here are no nested classes displayed

nested-classes-button **ON**  :

[![nestedclasses_on](http://i.imgur.com/xKIsKnIm.jpg)](http://i.imgur.com/xKIsKnI.jpg) here are the nested classes displayed


## Filtered for methods with refinements:

methods-with-refinements-filter **OFF** :                    
    
[![methods_refinements_off](http://i.imgur.com/EJLJ9bwm.jpg)](http://i.imgur.com/EJLJ9bw.jpg) Only methods without refinements are displayed

methods-with-refinements-filter **ON** :    
 
[![Methods_refinements_on](http://i.imgur.com/kHdFgd7m.jpg)](http://i.imgur.com/kHdFgd7.jpg) Methods without **and with** are displayed

##**Example project:**

[![example](http://i.imgur.com/fWFuEJDl.png)](http://i.imgur.com/fWFuEJD.png)