<!-- Breadcrumb -->
[**HOME**](https://github.com/FeatureIDE/FeatureIDE/wiki) < ... < [**Getting started**](https://github.com/FeatureIDE/FeatureIDE/wiki/Getting-started) < [**Preparing Eclipse**](https://github.com/FeatureIDE/FeatureIDE/wiki/Preparing-Eclipse)

<!-- Introduction -->

<!-- Outline -->

<!-- Content -->

1. You do not need to configure Eclipse yourself. We have prepackaged versions for all operating systems available on [our website]( https://featureide.github.io/#download). Download the latest version of "Eclipse with FeatureIDE, JDT, CDT, and AJDT". If you want to create your own version, or find out how we created these, check out the [FeatureIDE Installation and Update](https://github.com/FeatureIDE/FeatureIDE/wiki/FeatureIDE-Installation-and-Update) wiki page. 

2. Unzip eclipse into a folder where you have full permissions (it is recommended not to use the "program files" folder) 
3. Create shortcut to start eclipse with the folowing VM options:
 
   `- vmargs -Duser.name="Name Surname"`

   Alternatively, add the following line to `eclipse.ini`:

   `-Duser.name=Name Surname`
   
   Eclipse will automatically insert you name as author if you create a new Class

4. Start Eclipse and create a new workspace
   
   It is recommended to use a folder that is not indexed by Windows as this may cause interactions with git