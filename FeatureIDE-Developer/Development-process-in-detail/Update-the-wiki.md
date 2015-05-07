<!-- Breadcrumb -->
[**HOME**](https://github.com/tthuem/FeatureIDE/wiki) < [**FeatureIDE Developer**](https://github.com/tthuem/FeatureIDE/wiki/FeatureIDE-Developer) < [**Development Process in detail**](https://github.com/tthuem/FeatureIDE/wiki/Development-Process-in-detail)

<!-- Introduction -->
This page gives an overview of different topics like structure or guidelines which have to be considered for extensions of the FeatureIDE wiki. Wiki updates and extensions are very important because of the continuous development and evolution of FeatureIDE. It also helps the users and contributors to have an easy access to all functions of FeatureIDE and all changes since the initial version.

<!-- Outline -->
1. [Wiki Editing and Update Process] (#1-wiki-edit-and-update-process)
2. [Wiki Structure in General] (#2-wiki-structure-in-general)
	1. [Structure of folder and files and the table of contents] (#i-structure-of-folders-and-files-and-the-table-of-contents)
	2. [Naming Scheme] (#ii-naming-scheme)
	3. [Naming Conflicts] (#iii-naming-conflicts)
3. [Types and Structure of Wiki Pages] (#3-types-and-structure-of-wiki-pages)
	1. [Overview Page] (#3i-overview-page)
	2. [Details Page] (#3ii-detailed-page)
4. [Standard Page Elements] (#4-standard-page-elements)
	1. [Heading] (#i-heading)
	2. [Breadcrumb Navigation] (#ii-breadcrumb-navigation)
	3. [Images] (#iii-images)


<!-- Content -->
## 1. Wiki Edit and Update Process
One step of the development process is to edit or update one or more wiki pages. The pages and the amount of page updates are related to special topic, i.e. a ticket with an enhancement or error correction on which a FeatureIDE developer is currently working on. After the deployment of a FeatureIDE ticket, the wiki content has to be considered. The developer needs to check whether existing content has to be changed or new content is needed. In case the wiki page is incomplete or missing, an entirely new page or specific parts have to be created.

To have a consistent edit or update process it's necessary to work with a local copy of the wiki. Therefore you have to clone it from the git. To prevent errors in the file structure, we recommend to add a new page only after cloning the wiki repository locally. 

To work this way causes a disadvantage for windows users. Every change to the wiki has to be deployed and checked in the live system. There is a way for other OS to run the wiki locally. (https://github.com/gollum/gollum)

To clone the wiki locally, please follow the usual steps to clone a repository. For github wikis, there is only the opportunity to use an https-link. Nevertheless, the following link allows you to use ssh and prevents to provide user name and password every time you are pushing, pulling and so on:
ssh://git@github.com/tthuem/FeatureIDE.wiki.git

## 2. Wiki Structure in General
This section describes some basic topics concerning the structure of the FeatureIDE wiki.
### i. Structure of folders and files and the table of contents
The files and folders have to be synchronized with the structure of the topics in the table of contents (TOC) side to have an easier traceability of the specific pages. A page and its subpages are organized in a single folder (folder name = page name). A folder may also contain other folders to organize subpages. In general a depth of 3 is the maximum amount of sublevels for the TOC. To use a deeper structure it's necessary to follow the existing organization of folders and pages. In addition, you have to build a special TOC (_Sidebar.md) to cover all content on the levels 4 to 6 and please pay attention to the maximum depth of 3. The TOC is used for all files in the same folder and all folders underneath.

### ii. Naming Scheme
The name of a page file is decisive to the title shown on this page. It works based on the following scheme: "this-is-a-page-title" will be replaced with "this is a page title". Therefore, please take care about the correct name and spelling of the file name. 

### iii. Naming Conflicts
Naming conflicts occur if two pages have the same file name. The wiki needs unique names and ignores the folder structure at the same time. In the current version some of those section files exist. We need the same topic twice. One in each of both main sections. Therefore, we appended the suffix *-[FeatureIDE-Dev]* to each sub-element of the FeatureIDE developer main section.

## 3. Types and Structure of Wiki Pages
In the FeatureIDE wiki we differentiate two types of pages. The first one is an overview page to cover all information about a topic. It is used every time we going to branch into subtopics and therefore link into subsections. Those subsections may contain overview pages or concentrate on a special topic with all of its characteristics in a detailed page. The structure and used elements are described in the next two sections.

### 3.i. Overview Page
The overview pages are structured as follows:
* **Breadcrumb Navigation:**  We use a manually build breadcrumb navigation to have an easier overview of the page hierarchy and allows a quick navigation to a parent site. The concrete structure of the breadcrumb navigation is shown in section [4.ii] (#ii-breadcrumb-navigation)
* **Short Description:** This part of the page gives a short description of the content of the current page.
* **Quick Navigation:** As a central part of the overview page the quick navigation, especially the navigation table, is used to give an overview of the child pages. Therefore a table structure is used. 
  * If you create a new overview page it should be the easiest way to copy the html table from an existing page and modify it for the special needs. We are not using the markdown commands. The table is directly built in html.
  * The table has to be modified to have a fixed width in its tds. It has to be calculated based on the table width value of 640px. According to the amount of columns the table width is divided and rounded to have all parts of equal width. (640px/3 = 213,333 -> 213px)
  * If you want use more than five columns the content has to be spread into two separate tables. There are overview pages which use two of those tables you may take a look at and copying it.
  * Every subsection or subpage is represented by a column with the following rows:
    * Topic of the subsection. (Title of the page behind this topic)
	* Representative image for the topic. It may be difficult to create a matching image. Therefore it's meaningful to reuse an existing one or the "under construction" image in the root folder.
	* The third row covers a link to the subpage.
	* In the last row you have to provide a short description of the content of the subpage.
	
### 3.ii. Detailed Page
This page describes a topic in detail without further subpages and with a fixed structure:
* **Breadcrumb Navigation:**  We use a manually build breadcrumb navigation to have an easier overview of the page hierarchy and allows a quick navigation to a parent site. The concrete structure of the breadcrumb navigation is shown in section [4.ii] (#ii-breadcrumb-navigation)
* **Short Description:** This part of the page gives a short description of the content of the current page.
* **Outline:** Overview of the content structure by referencing the headings in the page. How to deal with headings and how to reference them is described in section [4.i.](#i-heading)
* **Content:** The content represents the main part of page.

The current page is an example for a detailed page.

## 4. Standard Page Elements
In this section we give an overview of some page elements to define the usage on the wiki pages.

### i. Heading
Headings are used in a depth with a maximum of 3 and begin at the markdown command ("##"). That's why the commands are used in the hierarchy "##, ###, ####". The headings on overview pages are not numbered. On a detailed page headings are used in a numbered way to build up a structured content. A heading isn't numbered automatically. 
The correct numbering has to be added manually based on the markdown numbering of the outline hierarchy (i.e. 2.i.b or 3.iv). The first level uses Arabic numbers followed by Latin numbers on the second level and small letters on the third level. 
A heading has to be extended by adding the correct numbering as prefix in front of the heading title (i.e. 1.i.b. is a heading on level three).

### ii. Breadcrumb Navigation
On every page a breadcrumb navigation is shown to provide an easier navigation to user. The breadcrumb has to be built manually and is based the following characteristics:
* **HOME** < **PPP** < **PP** < **P** It starts with a link to the wiki itself as HOME. Considering the site hierarchy every parent (P) or parent of the parent (PP) and so on is shown in the breadcrumb. 
* The breadcrumb navigation should be limited to a single line on the site. Therefore some parts of the hierarchy were left out. It's necessary to show the HOME link in front and the link to the direct parent and if it's possible higher parent (PP). 
* In case of hiding some levels they are substituted by "..." (i.e. HOME < ... < PP < P).

### iii. Images
Every image is saved in the Assets folder. The images are stored in a folder hierarchy, which should be identical to the wiki structure. If a folder is not present it has to be generated. In contrast to the pages of the FeatureIDE wiki the images are referenced with a deep link. This may lead to long image references but is necessary to have a traceability for images as well.



