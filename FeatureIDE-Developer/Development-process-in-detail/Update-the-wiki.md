<!-- Breadcrumb -->
[**HOME**](https://github.com/tthuem/FeatureIDE/wiki) < [**FeatureIDE Developer**](https://github.com/tthuem/FeatureIDE/wiki/FeatureIDE-Developer) < [**Development Process in detail**](https://github.com/tthuem/FeatureIDE/wiki/Development-Process-in-detail)

<!-- Introduction -->
This page gives an overview of different topics like structure or guidelines which have to be considered in the extension of the existing FeatureIDE wiki. The wiki extension or modification is an important part of the development process. A continuous development of the wiki is necessary to fill up all of the pages. It also helps the users and contributors to have an easy access to all of the aspects of FeatureIDE and all changes since the initial version of a wiki page has been created.

<!-- Outline -->
1. [Wiki editing and  update process] ()
	1. Structure of folder, files and table of contents ()
	2. Naming Scheme ()
	3. Naming conflict ()
2. [Wiki structure in general] ()
3. [Types of wiki pages] ()
4. [Standard page elements] ()
5. [Page structure] ()
	1. [Overview page] ()
	2. [Details page] ()

<!-- Content -->
## 1. Wiki edit and update process
In the development process one step is the edit or update of one or more pages of the wiki. The pages and the amount of page update are related to special topic, i.e. a ticket with an enhancement or error correction, a FeatureIDE developer is currently working at. After the deployment of the FeatureIDE code changes for the ticket, the wiki content has to considered, whether existing content has to be changed or in case the wiki page is incomplete or missing an entirely new page or specific parts have to be created.

To have a consistent edit or update process its necessary to work with a local copy of the wiki. Therefore you have to clone it from the git. To prevent errors in the file structure its considered to add new page only after cloning the wiki repository locally. 

To work this way causes a disadvantage for windows users. Every change to the wiki has to be deployed and checked in the live system. There is a way for other os to run the wiki locally. (https://github.com/gollum/gollum)

To clone the wiki locally follow the usual steps to clone a repository. On github only the https-link is given. 
Following link allows you to use ssh and prevents to provide username and password everytime you are pushing, pulling and so on:
ssh://git@github.com/tthuem/FeatureIDE.wiki.git

## 2. Wiki structure in general
This section describes some basic topics concerning the structure of the FeatureIDE wiki.
### i. Structure of folder, files and table of contents
The files and folders have to be synchronized with the structure of the topics in the table of contents (TOC) side to have an easier traceability of the specific pages. A page and its subpages are organized in a single folder named liked the page. A folder may also contain other folders to organize a subpage and its subsubpage. In general a depth of 3 the maximum amount of sublevels for the TOC. To use a deeper structure its necessary to follow the existing organization of folders and pages. Additional you have to build a special TOC (_Sidebar.md) to cover all of the content for the content on the levels 4 to 6 considering the maximum depth of 3 also. The TOC is used for all files in the same and underlying folders.

### ii. Naming Scheme
The name of a page file is decisive to the title shown on this page. It works based on the following scheme: "this-is-a-page-title" will be replaced with "this is a page title". That's why you have to take care of the correct name and spelling of the file name. 

### iii. Naming conflict
Naming conflicts occur if two pages have the same file name. The wiki needs unique names and ignores the folder structure at the same time. In the current version some of those section files exist. We need the same topic twice. One in each of both main sections. Therefore as a sub-element of the FeatureIDE developer main section the suffix *-[FeatureIDE-DEV]* is appended to the file name.


## 3. Types of wiki pages


## 4. Standard page elements


## 5. Page structure


### 5.i. Overview page


### 5.ii. Details page


