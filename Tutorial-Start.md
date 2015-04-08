# Getting started with FeatureIDE

This tutorial will help you to build your first FeatureIDE project. After you have finished this tutorial, you will have a simple *Hello World* software product line. If you have problemes at a certain step, you can get the final result using <code>File-> New-> Example</code> in Eclipse's main menu.
The first step for your product line is domain engineering. Here you think about what features to provide for your product.

**More Information:** For further information about software product line engineering use the help button. This picture will show you the basic idea between domain engineering and application engineering.

## Introduction
### Open the FeatureIDE perspective
When using FeatureIDE it is best to activate the FeatureIDE perspective. Thus, the first Next, create a new project. You can find the Feature IDE Project wizard under <code>File / New </code>. On the next page, choose a project name. For example <code>HelloWorld</code>;. Then, close the wizard by clicking *Finish*.
In the wizard you can select different composition engines. You can choose any composition engine but remember your decision. Because each composition engine is slight different in use, you have to choose your selection later in this tutorial.
**Info:** You can find a short introduction to alternative composition engines at the end of this cheat sheet.e first step is to switch the active perspective to the FeatureIDE Perspective. You can use the button on the upper right corner of the workbench or <code>Window / Open Perspective / Others...</code> and select Feature IDE. 
### Create a FeatureIDE Project
Next, create a new project. You can find the FeatureProject wizard under <code>File-> New</code>. You can also start the wizard by clicking on the button below.
In the wizard you can select different composition engines. You can choose any composition engine but remember your decision for later steps in this tutorial.
(You can find a short introduction to alternative composition engines at the end of this cheat sheet)
On the next page, choose a project name. For example *"HelloWorld"*. Then, close the wizard by clicking *Finish*. 
## Create a feature model
Now its time to create a feature model specifying the features and their valid combinations.

1. After creation of the project, FeatureIDE opens the <code>model.xml</code> file. You will see a graphical editor where you can edit the feature model of your software product line.

First, create two additional layers under your root feature. Right click on the root feature and select <code>Create Feature (below)</code> twice. Rename the first new feature to <code>Hello</code>, and the second to <code>World</code>. You can rename features using **F2**, a single click on a selected feature, or using a right click with the option at the context menu.

2. Rename the feature <code>Base</code> to <code>Beautiful</code> and move it between the features <code>Hello</code> and <code>World</code>. Now, create a feature <code>Wonderful</code> and move it between the features <code>Beautiful</code> and <code>World</code>.

3. Now, we want to make the features <code>Beautiful</code> and <code>Wonderful</code> exclusive to each other. Select both features, create a new compound above using right click menu, and name it <code>Feature</code>. As this feature has no according implementation mark it as abstract using the context menu.

4. Connections between feature and its group of children are distinguished as **And**- (no arc), **Or**- (filled ar) and **Alternative**-groups (unfilled arc). 

The children of And-groups can either be **mandatory** (filled circle) or **optional** (unfilled circle).

5. Double click on the connection below the feature <code>Feature</code> to change it to an *Or*-group and again to change it to an *Alternative*-group. Then double click on the features <code>Hello</code> and <code>World</code> to mark them as *mandatory*. Click on the help button, to see how your feature model should look like. 

## Implementing features
It is now time to implement the features. The implementation details depend on the composer you have chosen. Please select the task that explains the implementation for the composer you have chosen during project creation.

### AHEAD
This tutorial guides you through the implementation of features using AHEAD. It supports composition of <code>Jak</code> files. <code>Jak</code> extends Java with keywords for Feature-Oriented-Programming which are
* <code>refines</code>: used to specify refinements of an existing class. 
* <code>Super()</code>: used to call a refined method . 

#### Create new JAK files
After you have saved your feature model, FeatureIDE will create directories for each feature. In these directories you can create <code>Jak</code>-Files.
Start with creating a new <code>Jak</code>-file in the directory <code>Hello</code>.
Right click on the directory <code>Hello</code> and use the command <code>New / FeatureIDE File</code> of the popup menu. Choose the identifier <code>Main</code> for the class name and press the *Finish* button.
FeatureIDE opens the file and you can write the following code:
``` Java
public void print(){
   System.out.print("Hello");
}

public static void main(String[] args) {
   new Main().print();
} 
```

Now create more <code>Jak</code> files, one in each of the directories <code>Beautiful</code>, <code>Wonderful</code> and <code>World</code>. In these cases, activate the option **Refines** in the Wizard. Furthermore, all the <code>Jak</code> files must have the same name <code>Main</code>.

#### Source code for the JAK files
Now edit the remaining <code>Jak</code>-Files. Every feature will refine the method <code>print()</code> in the class <code>Main</code>.

Now insert the following code in your world feature: 
``` Java
public void print() {
   Super().print();
   System.out.print(" world!");
}
```

In the other files you can insert the same code and just change the print method.

**Example**
``` Java
System.out.print(" wonderful") // in the "Wonderful" feature.
System.out.print(" beautiful") // in the "Beautiful" feature. 
```
### FeatureC++
FeatureC++ is a C++ language extension to support Feature-Oriented Programming (FOP). The extension of C++ is similar to the Java extension (Jak) by AHEAD with the new keywords:
* <code>refines</code>: used to specify refinements of an existing class. 
* <code>super</code>: used to call a refined method . 

After you have saved your feature model, FeatureIDE will create directories for each feature. In these directories you can create <code>cpp</code>-Files.

#### Create new cpp files
Start with creating a new <code>cpp</code>-file in the directory <code>Hello</code>: *Right click* on the directory and use the item <code>New / FeatureIDE File</code>. Choose the identifier <code>"Main"</code> for the class name and press the *Finish* button.

FeatureIDE opens the file and you can write the following code:

``` CPP
#include "stdio.h"
class Main {
   public:
   int run() { 
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
```

Now create more <code>cpp</code> files, one in each of the directories <code>Beautiful</code>, <code>Wonderful</code> and <code>World</code>. In these cases, activate the option **Refines** in the Wizard. Furthermore, all the <code>cpp</code> files must have the same name <code>Main</code>.

#### Source code for the cpp-files
Now edit the remaining <code>cpp</code>-Files. Every feature will refine the method <code>print()</code> in the class <code>Main</code>.

Now insert the following code in your world feature: 

``` CPP
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
```

In the other files you can insert the same code and just change the print method.

**Example:**
``` CPP
printf(" wonderful"); in feature "Wonderful".
printf(" beautiful"); in feature "Beautiful". 
```

### FeatureHouse
FeatureHouse is language-independent in that software artifacts written in various languages can be composed, e.g., source code, test cases, models, documentation, makefiles. Currently, FeatureHouse provides support for the composition of software artifacts written in Java, C#, C, Haskell, JavaCC, Alloy and UML. In this tutorial you will use Java.

#### Create new Java files
After you have saved your feature model, FeatureIDE will create directories for each feature automatically. In these directories you can create <code>Java</code>-Files.
Start with creating a new <code>Java</code>-file in the directory <code>Hello</code> by right clicking on the directory and use the context-item <code>New / FeatureIDE File</code>. Choose the identifier <code>Main</code> for the class name and press *Finish* button.

FeatureIDE opens the file and you can write the following code: 

``` Java
public class Main {
   protected void print() {
      System.out.print("Hello");
   }

   public static void main(String[] args){
      new Main().print();
   }
}
```

Now create more <code>Java</code> files. Create one in each of the directories <code>Beautiful</code>, <code>Wonderful</code> and <code>World</code>. In these cases, activate the option **Refines** in the Wizard. Furthermore, all the <code>Java</code> files must have the same name <code>Main</code>.

#### Source code for the Java-files
Now edit the remaining <code>Java</code>-Files. Every feature will refine the method <code>print()</code> in the class <code>Main</code>.

Now insert the following code in your world feature: 

``` Java
public class Main {
   protected void print() {
      original();
      System.out.print(" World!");
   }
}
```

In the other files you can insert the same code and just change the print method.

**Example:**
``` Java
System.out.print(" wonderful"); // in feature "Wonderful".
System.out.print("beautiful"); // in feature "Beautiful". 
```

### AspectJ
AspectJ is a aspect-oriented extension of Java. 

#### Create a new base program
In FeatureIDE each feature corresponds to one aspect. First create the <code>Java</code> files for your base program. The aspects for each feature are created automatically. Start with creating a new <code>Java</code>-file in the <code>src</code>-directory by right clicking on the directory and choose to create a <code>new Java class</code>. Choose the identifier <code>Main</code> for the class name and press *Finish* button.

FeatureIDE opens the file and you can write the following code:

``` Java
public void print(){
   System.out.print("Hello");
}

public static void main(String[] args) {
   new Main().print();
} 
```

#### Source code for the aspects
Now edit the existing aspects (<code>.aj</code>) for each feature. Every feature will refine the method <code>print()</code> in the class <code>Main</code>.

Now insert the following code in your world feature: 

``` Java
public aspect Wonderful {
   after(): call(void Main.print()) {
      System.out.print(" wonderful");
   }
}
```

In the other files you can insert the same code and just change the print method.

**Example:**
``` Java
System.out.print(" wonderful"); // in the "Wonderful" feature.
System.out.print(" beautiful"); // in the "Beautiful" feature. 
```
### DeltaJ
DeltaJ is a Java-like language supporting Delta-Oriented-Programming. Delta-Oriented-Programming is similar to Feature-Oriented-Programming but each project contains of one core module and a set of delta modules. A core module is a simple collection of classes, while a delta module is a set of operations that allow to add a new class and modify or remove classes declared in other delta or core modules. Keywords: 
* <code>modifies</code>: used to specify a refined class or 
* method <code>original()</code>: used to call a refined method 
* <code>delta</code>: used to specify a delta module 
* <code>core</code>: used to specify a core module 
* <code>after</code>: used to specify module dependencies (the current module depends on the list of modules following the after keyword) 

**Example:**
``` Java
delta Wonderful after Beautiful when Wonderful{ 
   modifies class Main{ 
      modifies void print() { 
         original(); 
         new SystemOutWrapper().print(" wonderful"); 
      } 
   } 
} 
```

**NOTE**: a core module includes a lines specifying features and configurations. In FeatureIDE these lines are modified automatically. 


### Munge
Munge is a purposely-simple Java preprocessor. When using Munge you can use Munge-style Java comments to specify the mapping between parts of code and features.

#### Implement your Munge product line

**Example:**

``` Java
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
```

### Antenna
Antenna is a Java preprocessor. You can use Antenna-style Java comments to specify the mapping between parts of code and features. 

#### Implement your Antenna product line

**Example:**

``` Java
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
}
```

## Creating a configuration

In this part of the tutorial you will create your first configuration.

### The configuration file
After you designed your feature model, and source code, you want to generate a variant which is a product of your product line. To specify a variant, you have to provide a feature selection. This is done in a per-variant configuration file 

Create a new configuration file with the according wizard. 

Open the configuration file and select the features you want to activate for your variant. After you have saved the file, FeatureIDE will compose your features and compile the generated Java code.

### Start your application
Now it's time to start your application. Right click on the project in package explorer and choose <code>Run As > Java Application</code>. Choose a class name without <code>$$</code> in the name and enjoy your *Hello Beautiful Wonderful Word* application! The next time you want to start your application simply use the run button in the eclipse tool bar. 

## What's next?

### Checkout our examples

You can access our examples using 
- <code>New / Examples...</code> in package explorer or via 
- <code>File / New -> Others</code> in Eclipse main menu by selecting <code>Feature IDE -> Feature IDE Examples</code> under the node Examples the dialog's tree control. 

We provide a *HelloWorld* example for every FeatureIDE extension, which may help to create projects in other languages and with other composition mechanisms. 




