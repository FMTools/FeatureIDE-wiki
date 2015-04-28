<!-- Breadcrumb -->
[**HOME**](https://github.com/tthuem/FeatureIDE/wiki) < [**FeatureIDE Developer**](https://github.com/tthuem/FeatureIDE/wiki/FeatureIDE-Developer) < [**Development Process in detail**](https://github.com/tthuem/FeatureIDE/wiki/Development-Process-in-detail)

<!-- Introduction -->
This page gives an overview of different topics like structure or guidelines which have to be considered in the extension of the existing FeatureIDE wiki. The wiki extension or modification is an important part of the development process. A continuous development of the wiki is necessary to fill up all of the pages. It also helps the users and contributors to have an easy access to all of the aspects of FeatureIDE and all changes since the initial version of a wiki page has been created.

<!-- Outline -->
1. [Wiki editing and  update process] (#1-wiki-edit-and-update-process)
2. [Wiki structure in general] (#2-wiki-structure-in-general)
	1. [Structure of folder and files and the table of contents] (#i-structure-of-folders-and-files-and-the-table-of-contents)
	2. [Naming Scheme] (#ii-naming-scheme)
	3. [Naming conflicts] (#iii-naming-conflicts)
3. [Types and structure of wiki pages] (#3-types-and-structure-of-wiki-pages)
	1. [Overview page] (#3i-overview-page)
	2. [Details page] (#3ii-detailed-page)
4. [Standard page elements] (#4-standard-page-elements)
	1. [Heading] (#i-heading)
	2. [Breadcrumb navigation] (#ii-breadcrumb-navigation)
	3. [Images] (#iii-images)


<!-- Content -->
## 1. Wiki edit and update process
In the development process one step is the edit or update of one or more pages of the wiki. The pages and the amount of page update are related to special topic, i.e. a ticket with an enhancement or error correction, a FeatureIDE developer is currently working at. After the deployment of the FeatureIDE code changes for the ticket, the wiki content has to considered, whether existing content has to be changed or in case the wiki page is incomplete or missing an entirely new page or specific parts have to be created.

To have a consistent edit or update process its necessary to work with a local copy of the wiki. Therefore you have to clone it from the git. To prevent errors in the file structure its considered to add new page only after cloning the wiki repository locally. 

To work this way causes a disadvantage for windows users. Every change to the wiki has to be deployed and checked in the live system. There is a way for other OS to run the wiki locally. (https://github.com/gollum/gollum)

To clone the wiki locally follow the usual steps to clone a repository. On github only the https-link is given. 
Following link allows you to use ssh and prevents to provide user name and password every time you are pushing, pulling and so on:
ssh://git@github.com/tthuem/FeatureIDE.wiki.git

## 2. Wiki structure in general
This section describes some basic topics concerning the structure of the FeatureIDE wiki.
### i. Structure of folders and files and the table of contents
The files and folders have to be synchronized with the structure of the topics in the table of contents (TOC) side to have an easier traceability of the specific pages. A page and its subpages are organized in a single folder named liked the page. A folder may also contain other folders to organize a subpage and its subsubpage. In general a depth of 3 the maximum amount of sublevels for the TOC. To use a deeper structure its necessary to follow the existing organization of folders and pages. Additional you have to build a special TOC (_Sidebar.md) to cover all of the content for the content on the levels 4 to 6 considering the maximum depth of 3 also. The TOC is used for all files in the same and underlying folders.

### ii. Naming Scheme
The name of a page file is decisive to the title shown on this page. It works based on the following scheme: "this-is-a-page-title" will be replaced with "this is a page title". That's why you have to take care of the correct name and spelling of the file name. 

### iii. Naming conflicts
Naming conflicts occur if two pages have the same file name. The wiki needs unique names and ignores the folder structure at the same time. In the current version some of those section files exist. We need the same topic twice. One in each of both main sections. Therefore as a sub-element of the FeatureIDE developer main section the suffix *-[FeatureIDE-Dev]* is appended to the file name.

## 3. Types and structure of wiki pages
In the FeatureIDE wiki we differentiate two types of pages. The first one is an overview page to cover all information about a topic and is used every time we going to branch into subtopics and therefore link into subsections. Those subsections may contain overview pages or concentrate on a special topic with all of its characteristics in a detailed page. The structure and used elements are described in the next two sections.

### 3.i. Overview page
The overview pages are structured as follows:
* **Breadcrumb navigation:**  We use a manually build breadcrumb navigation to have an easier overview of the page hierarchy and allows a quick navigation to a parent site. The concrete structure of the breadcrumb navigation is shown in section [4.ii] (#ii-breadcrumb-navigation)
* **Short description:** This part of the page gives a short description of the content of the current page.
* **Quick navigation:** As a central part of the overview page the quick navigation, especially the navigation table, is used to give an overview of the child pages. Therefore a table structure is used. It contains the following informations.
  * If you create a new overview page it should be the easiest way to copy the html table from an existing page and modify it for the special needs. We are not using the markdown commands. The table is directly build in html.
  * The table has to be modified to have a fixed width in its tds. It has to be calculated based on the table width value of 640px. According to the amount of columns the table with is divided and rounded to have all parts of equal width. (640px/3 = 213,333 -> 213px)
  * If you want use more than five columns the content has to be spread into two separate tables. There are overview pages which use two of those tables you may take a look at and copying it.
  * Every subsection or subpage you want to lead to is represented by a column with the following rows:
    * Topic of the subsection. (Title of the page behind this topic)
	* Representative image for the topic. It may be difficult to create a matching image. Therefore its meaningful to reuse an existing one or the "under construction" image in the root folder.
	* The third row covers a link to the subpage.
	* In the last row you have to provide a short description of the content of the subpage.
	
### 3.ii. Detailed page
Such a page describes a topic in detail. This page has no subpages and is based on a fixed structure also:
* **Breadcrumb navigation:**  We use a manually build breadcrumb navigation to have an easier overview of the page hierarchy and allows a quick navigation to a parent site. The concrete structure of the breadcrumb navigation is shown in section [4.ii] (#ii-breadcrumb-navigation)
* **Short description:** This part of the page gives a short description of the content of the current page.
* **Outline:** Overview of the content structure by referencing the headings in the page. How to deal with headings and how to reference them is described in section [4.i.](#i-heading)
* **Content:** The content represents the main part of page.

The current page is an example for a detailed page.

## 4. Standard page elements
In this section we give an overview of some page elements to define the usage on the wiki pages.

### i. Heading
Headings are used in a depth with a maximum of 3 and begin at the markdown command ("##"). That's why the commands are used in the hierarchy "##, ###, ####". The headings on overview pages are not numbered. On a detailed page headings are used in a numbered way to build up a structured content. A heading isn't numbered automatically. 
The correct numbering has to be added manually based on the markdown numbering of the outline hierarchy (i.e. 2.i.b or 3.iv). The first level uses Arabic numbers followed by Latin numbers on the second level and small letters on the third level. 
A heading has to be extended by adding the correct numbering as prefix in front of the heading title (i.e. 1.i.b. this a heading on level three).

### ii. Breadcrumb navigation
On every page a breadcrumb navigation is shown to provide an easier navigation to user. The breadcrumb has to be build manually and is based the following characteristics:
* **HOME** < **PPP** < **PP** < **P** It starts with a link to the wiki itself as HOME. Considering the site hierarchy every parent (P) or parent of the parent (PP) and so on is shown in the breadcrumb. 
* The breadcrumb navigation should be limited to a single line on the site. Therefore some parts of the hierarchy were left out. It's necessary to show the HOME link in front and the link to the direct parent and if it's possible higher parent (PP). 
* In case of hiding some levels they are substituted by "..." (i.e. HOME < ... < PP < P).

### iii. Images
Every image is saved in the Assets folder. The images are stored in a folder hierarchy, which should be identical to the wiki structure. If a folder is not present it has to be generated. In contrast to the pages of the FeatureIDE wiki the images are referenced with a deep link. This may lead to long image references but is necessary to have a traceability for images as well.



