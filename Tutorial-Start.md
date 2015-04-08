# Getting started with FeatureIDE

This tutorial will help you to build your first FeatureIDE project. After you have finished this tutorial, you will have a simple *Hello World* software product line. If you have problemes at a certain step, you can get the final result using <code>File-> New-> Example</code> in Eclipse's main menu.
The first step for your product line is domain engineering. Here you think about what features to provide for your product.
More Information: For further information about software product line engineering use the help button. This picture will show you the basic idea between domain engineering and application engineering.

## Introduction
### Open the FeatureIDE perspective
When using FeatureIDE it is best to activate the FeatureIDE perspective. Thus, the first Next, create a new project. You can find the Feature IDE Project wizard under File-&gt; New. On the next page, choose a project name. For example &quot;HelloWorld&quot;. Then, close the wizard by clicking Finish.
In the wizard you can select different composition engines. You can choose any composition engine but remember your decision. Because each composition engine is slight different in use, you have to choose your selection later in this tutorial.
Info: You can find a short introduction to alternative composition engines at the end of this cheat sheet.e first step is to switch the active perspective to the FeatureIDE Perspective. You can use the button on the upper right corner of the workbench or Window / Open Perspective / Others... and select Feature IDE. 
### Create a FeatureIDE Project
Next, create a new project. You can find the FeatureProject wizard under File-> New. You can also start the wizard by clicking on the button below (Click to perform).
In the wizard you can select different composition engines. You can choose any composition engine but remember your decision for later steps in this tutorial.
(You can find a short introduction to alternative composition engines at the end of this cheat sheet)
On the next page, choose a project name. For example "HelloWorld". Then, close the wizard by clicking Finish. 
## Create a feature model
Now its time to create a feature model specifying the features and their valid combinations.

1. After creation of the project, FeatureIDE opens the model.xml file. You will see a graphical editor where you can edit the feature model of your software product line.

First, create two additional layers under your root feature. Right click on the root feature and select "Create Feature (below)" twice. Rename the first new feature to "Hello", and the second to "World". You can rename features using F2, a single click on a selected feature, or using a right click with the option at the context menu.

2. Rename the feature (Base) to >Beautiful> and move it between the features (Hello) and (World). Now, create a feature (Wonderful) and move it between the features (Beautiful) and (World).

3. Now, we want to make the features (Beautiful) and (Wonderful) exclusive to each other. Select both features, create a new compound above using right click menu, and name it (Feature). As this feature has no according implementation mark it as abstract using the context menu.

4. Connections between feature and its group of children are distinguished as And- (no arc), Or- (filled ar) and Alternative-groups (unfilled arc). The children of And-groups can either be mandatory (filled circle) or optional (unfilled circle).

5. Double click on the connection below the feature (Feature) to change it to an Or-group and again to change it to an Alternative-group. Then double click on the features (Hello) and (World) to mark them as mandatory. Click on the help button, to see how your feature model should look like. 

## Implementing features
### AHEAD
This tutorial guides you through the implementation of features using AHEAD.

It is now time to implement the features. The implementation details depend on the composer you have chosen. Please select the task that explains the implementation for the composer you have chosen during project creation.

#### Create new JAK files
After you have saved your feature model, FeatureIDE will create directories for each feature. In these directories you can create Jak-Files.
Start with creating a new Jak-file in the directory "Hello"
Right click on the directory "Hello" and use the command New->FeatureIDE File of the popup menu. Choose the identifier "Main" for the class name and press the Finish button.
FeatureIDE opens the file and you can write the following code:
public void print(){
System.out.print("Hello");
}
public static void main(String[] args) {
new Main().print();
} 

Now create more Jak files, one in each of the directories "Beautiful";, "Wonderful"; and "World". In these cases,  activate the option "Refines"; in the Wizard. Furthermore, all the Jak files must have the same name Main.

#### Source code for the JAK files
Now edit the remaining jak-Files. Every feature will refine the method print() in the class Main.
Now insert the following code in your world feature: 
public void print() {
Super().print();
System.out.print(" world!");
}
In the other files you can insert the same code and just change the print method.
For example:
System.out.print(" wonderful"); in the "Wonderful" feature.
System.out.print(" beautiful");
in the "Beautiful" feature. 

### FeatureC++
It is now time to implement the features. The implementation details depend on the composer you have chosen. Please select the task that explains the implementation for the composer you have chosen during project creation.

#### Create new cpp files
After you have saved your feature model, FeatureIDE will create directories for each feature. In these directories you can create cpp-Files.
Start with creating a new cpp-file in the directory Hello: Right click on the directory and use the item New -> FeatureIDE File. Choose the identifier "Main" for the class name and press the Finish button.
FeatureIDE opens the file and you can write the following code:
#include "stdio.h"
class Main {"
public:"
int run() { "
printf("Hello");
return 0;
}
};
int main() {
//create instance of "Main"
Main myHello;
//run Main::run as entry-point of the app
return myHello.run();
}

Now create more cpp files, one in each of the directories "Beautiful", "Wonderful" and "World". In these cases,  activate the option "Refines" in the Wizard. Furthermore, all the cpp files must have the same name Main.

#### Source code for the cpp-files
Now edit the remaining cpp-Files. Every feature will refine the method print() in the class Main.
Now insert the following code in your world feature: 
refines class Main {
public:
int run() { 
int res = super::run(); 
if (res!=0)
return res;
printf(" World!");
return 0;
}
};
In the other files you can insert the same code and just change the print method.
Example:
printf(" wonderful"); in feature "Wonderful".
printf(" beautiful"); in feature "Beautiful". 

### FeatureHouse
It is now time to implement the features. The implementation details depend on the composer you have chosen. Please select the task that explains the implementation for the composer you have chosen during project creation
#### Create new Java files
FeatureHouse is language-independent in that software artifacts written in various languages can be composed, e.g., source code, test cases, models, documentation, makefiles. Currently, FeatureHouse provides support for the composition of software artifacts written in Java, C#, C, Haskell, JavaCC, Alloy and UML.
In this tutorial you will use Java.
After you have saved your feature model, FeatureIDE will create directories for each feature automatically. In these directories you can create Java-Files.
Start with creating a new Java-file in the directory Hello by right clicking on the directory and use the context-item New -> FeatureIDE File. Choose the identifier "Main" for the class name and press Finish button.
FeatureIDE opens the file and you can write the following code: 
public class Main {
protected void print() {
System.out.print("Hello");
}
public static void main(String[] args){
new Main().print();
}
}

Now create more Java files. Create one in each of the directories "Beautiful", "Wonderful"; and "World";. In these cases,  activate the option "Refines"; in the Wizard. Furthermore, all the Java files must have the same name Main.

#### Source code for the Java-files
Now edit the remaining java-Files. Every feature will refine the method print() in the class Main.
Now insert the following code in your world feature: 
public class Main {
protected void print() {
original();
System.out.print(" World!");
}
}
In the other files you can insert the same code and just change the print method.
Example:
System.out.print(" wonderful"); // in feature "Wonderful".
System.out.print("beautiful"); // in feature "Beautiful". 

### AspectJ
It is now time to implement the features. The implementation details depend on the composer you have chosen. Please select the task that explains the implementation for the composer you have chosen during project creation.

#### Create a new base program
AspectJ is a aspect-oriented extension of Java. In FeatureIDE each feature corresponds to one aspect. 
First create the Java files for your base program. The aspects for each feature are created automatically. Start with creating a new Java-file in the src-directory by right clicking on the directory and choose to create a new Java class. Choose the identifier "Main" for the class name and press Finish button.
FeatureIDE opens the file and you can write the following code:
public void print(){
System.out.print("Hello");
}
public static void main(String[] args) {
new Main().print();
} 

#### Source code for the aspects
Now edit the existing aspects (.aj) for each feature. Every feature will refine the method print() in the class Main.
Now insert the following code in your world feature: 
public aspect Wonderful {
after(): call(void Main.print()) {
System.out.print(" wonderful");
}
}
In the other files you can insert the same code and just change the print method.
Example:
System.out.print(" wonderful"); // in the "Wonderful" feature.
System.out.print(" beautiful"); // in the "Beautiful" feature. 

### Munge
It is now time to implement the features. The implementation details depend on the composer you have chosen. Please select the task that explains the implementation for the composer you have chosen during project creation.

#### Implement your Munge product line

Munge is a purposely-simple Java preprocessor. When using Munge you can use Munge-style Java comments to specify the mapping between parts of code and features.
Example:
public class Main {
public static void main(String[] args){
/*if[Hello]*/
System.out.print("Hello");
/*end[Hello]*/
/*if[Beautiful]*/ 
System.out.print(" beautiful");
/*end[Beautiful]*/
/*if[Wonderful]*/ 
System.out.print(" wonderful"); 
/*end[Wonderful]*/
/*if[World]*/ 
System.out.print(" world!");
/*end[World]*/
}
}


### Antenna
It is now time to implement the features. The implementation details depend on the composer you have chosen. Please select the task that explains the implementation for the composer you have chosen during project creation.

#### Implement your Antenna product line

Antenna
Antenna is a Java preprocessor. You can use Antenna-style Java comments to specify the mapping between parts of code and features.
Example:
//#if Hello
System.out.print("Hello");
//#endif
//#if Beautiful
System.out.print(" beautiful");
//#endif
//#if Wonderful
System.out.print(" wonderful"); 
//#endif
//#if World
System.out.print(" world!");
//#endif
t(" world!");
//#endif
}

## Creating a configuration

In this part of the tutorial you will create your first configuration.

### The configuration file
After you designed your feature model, and source code, you want to generate a variant which is a product of your product line. To specify a variant, you have to provide a feature selection. This is done in a per-variant configuration file 
Create a new configuration file with the according wizard. 

Open the configuration file and select the features you want to activate for your variant. After you have saved the file, FeatureIDE will compose your features and compile the generated Java code.

### Start your application
Now it's time to start your application. Right click on the project in package explorer and choose "Run As>Java Application". Choose a class name without "$$" in the name and enjoy your Hello Beautiful Wonderful Word application! The next time you want to start your application simply use the run button in the eclipse tool bar. 

## What's next?

### Checkout our examples

You can access our examples using 
- New -> Examples... in package explorer or via 
- File -> New -> Others in Eclipse main menu by selecting Feature IDE / Feature IDE Examples under the node Examples the dialog's tree control. 
We provide an HelloWorld example for every FeatureIDE extension, which may help to create projects in other languages and with other composition mechanisms. 

### Composer Overview

You have already learned how to create a FeatureIDE project that uses the AHEAD composer. In FeatureIDE you can also use FeatureC++, FeatureHouse, AspectJ, DeltaJ, Munge, and Antenna. The following section gives a short introduction to each of them. 

#### AHEAD 
You have already used the AHEAD composer in the FeatureIDE tutorial. It supports composition of Jak files. Jak extends Java with keywords for Feature-Oriented-Programming. Keywords: refines: used to specify refinements of an existing class. Super(): used to call a refined method . Example: public refines class Main { public void print() { Super().print(); System.out.print(" world!"); } } 

#### FeatureC++ 
FeatureC++ is a C++ language extension to support Feature-Oriented Programming (FOP). The extension of C++ is similar to the Java extension (Jak) by AHEAD. Keywords: refines: used to specify refinements of an existing class. super: used to call a refined method . Example: refines class Main { public: int run() { int res = super::run(); if (res!=0) return res; printf(" World!"); return 0; } }; 

#### FeatureHouse 
FeatureHouse is language-independent in that software artifacts written in various languages can be composed, e.g., source code, test cases, models, documentation, makefiles. Currently, FeatureHouse provides support for the composition of software artifacts written in Java, C#, C, Haskell, JavaCC, Alloy and UML. Keywords: original(): used to call a refined method. Example: (Java) public class Main { protected void print() { original(); System.out.print(" World!"); } } 

#### AspectJ 
AspectJ is a aspect-oriented extension of Java. In FeatureIDE each feature corresponds to one aspect. Example: public aspect Wonderful { after(): call(void Main.print()) { System.out.print(" wonderful"); } } 
DeltaJ DeltaJ is a Java-like language supporting Delta-Oriented-Programming. Delta-Oriented-Programming is similar to Feature-Oriented-Programming but each project contains of one core module and a set of delta modules. A core module is a simple collection of classes, while a delta module is a set of operations that allow to add a new class and modify or remove classes declared in other delta or core modules. Keywords: modifies: used to specify a refined class or method original(): used to call a refined method delta: used to specify a delta module core: used to specify a core module after: used to specify module dependencies (the current module depends on the list of modules following the after keyword) Example: delta Wonderful after Beautiful when Wonderful{ modifies class Main{ modifies void print() { original(); new SystemOutWrapper().print(" wonderful"); } } } NOTE: a core module includes a lines specifying features and configurations. In FeatureIDE these lines are modified automatically. 

#### Munge 
Munge is a purposely-simple Java preprocessor. When using Munge you can use Munge-style Java comments to specify the mapping between parts of code and features. Example: public class Main { public static void main(String[] args){ /*if[Hello]*/ System.out.print("Hello"); /*end[Hello]*/ /*if[Beautiful]*/ System.out.print(" beautiful"); /*end[Beautiful]*/ /*if[Wonderful]*/ System.out.print(" wonderful"); /*end[Wonderful]*/ /*if[World]*/ System.out.print(" world!"); /*end[World]*/ } } 

#### Antenna 
Antenna is a Java preprocessor. You can use Antenna-style Java comments to specify the mapping between parts of code and features. Example: //#if Hello System.out.print("Hello"); //#endif //#if Beautiful System.out.print(" beautiful"); //#endif //#if Wonderful System.out.print(" wonderful"); //#endif //#if World System.out.print(" world!"); //#endif } 
