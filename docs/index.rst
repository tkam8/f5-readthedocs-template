.. You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

F5 RTD Documentation Index
==============================================

Sample **docs** Folder Hierarchy
--------------------------------
This repo uses below folder hierarchy to provide an example structure for your guide. You can modify as needed. 
Reference: https://sphinx-rtd-tutorial.readthedocs.io/en/latest/folders.html 

- class1: Environment Setup
       - module1: GitHub Setup & Create new repository
       - module2: Read The Docs Setup
       - module3: Sourcetree Setup
       - module4: VS Code Setup
- class2: Clone Template and Edit Content 
       - module1: Clone to Local
       - module2: Edit Content
       - module3: reStructuredText overview
- class3: Commit Changes and Confirm Webpage
       - module1: Confirm and Commit Changes from Sourcetree
       - module2: Confirm build and Document in Read the Docs

About the `table of contents <https://docs.typo3.org/typo3cms/HowToDocument/WritingReST/MenuHierarchy.html>`__ syntax (view the raw format of this page to see code):
  - Default top level page with information about your project and table of contents. You must include the ``.. toctree::`` directive to tell Sphinx about the hierarchy structure of your sub-pages
  - titlesonly displays just the main title in the toc, not the sub sections
  - maxdepth tells sphinx how many sub-levels there are
  - caption is the name that will be displayed above your toc
  - glob will read all files specified and automatically create a menu. Use asterisks to match multiple files

Other files and folder in this **doc** directory:
------------------------------------

.. NOTE::
   The below files are required by Sphinx. Modify as instructed below to customize for your project. 

docs/**conf.py** 
~~~~~~~~~~~~~~~~~~
Python configuration file used by Sphinx (documentation tool). Make below arguments to customize this file.

- classname (line 8): This is the name of your lab, used in multiple areas like when creating a pdf
- github_url (line 76): The location of your github repo, displayed as the "Edit on GitHub" hyperlink in the html body
- project (line 154): This is the name of the project, used when printing pdf or epub

docs/**Makefile** and **make.bat**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
**No modification needed**. Used to set variables that define the location relevant files. Modify below arguments to customize this file.

docs/**preamble.tex**
~~~~~~~~~~~~~~~~~~~~~~~
**No modification needed**. Used to define the look and feel of the pdf version of your document. Used by LaTex. 

docs/**_static**
~~~~~~~~~~~~~~~~~~
**No modification needed**. Folder that stores static graphics and css files for your theme. 

docs/**_templates**
~~~~~~~~~~~~~~~~~~~~~
**No modification needed**. Folder that stores files that can be used to overwrite theme files for more customizability.
Current contents use the `F5 clouddocs <https://clouddocs.f5.com/>`__ theme. 

docs/**class1**
~~~~~~~~~~~~~~~~~
First folder (lab) of your training guide

- Contains class1.rst and intro.rst
       - class1.rst contains a more detailed description of the lab/guide as well as prerequisites if applicable. Also contains a toctree for sub-pages
       - intro.rst may contain a more detailed explanation of the content, infrastructure details and definition of terms used in the guide.
- Create **images** as needed
- Create **module** folders to hold content for sub labs/tasks


.. toctree::
   :titlesonly:
   :maxdepth: 2
   :caption: Contents:
   :glob:

   intro
   class*/class*
   module*/module*
