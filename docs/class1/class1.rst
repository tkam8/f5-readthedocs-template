Environment Setup
================================================

**Goal**: 
----------------
To set up your environment so you can use all the resources needed to create your documentation: GitHub, Sourcetree, VS Code, and Read the Docs. 

**Prerequisites**: 
------------------
- Windows or Mac with Internet Access
- Admin rights to install applications on your PC

Other files and folder in this directory:
------------------------------------

docs/**class1**/**workflow.rst** 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Displays the overall workflow used to create your document. 

docs/**class1**/**images**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Folder used to store images used in class1, used in class1.rst or intro.rst.  

.. toctree::
   :titlesonly:
   :maxdepth: 2
   :caption: Contents:
   :glob:

   workflow
   module*/module*
   


