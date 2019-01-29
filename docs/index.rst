.. You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome Page For Your F5 RTD Documentation!
==============================================

This template will help you create documentation based on `Sphinx <http://www.sphinx-doc.org/en/master/>`__ documentation generation tool. It uses `reStructuredText <http://docutils.sourceforge.net/rst.html>`__ markup language to modify the text as you see it on this page. 
Clone this repository using SourceTree as the Git client, modify the content, then change the origin to your own new remote (on GitHub) repository that will manage your own content. 

About this page (index.rst):
  - Default top level page with information about your project and table of contents. You must include the ``.. toctree::`` directive to tell Sphinx about the hierarchy structure of your sub-pages. 
  - maxdepth tells sphinx how many sub-levels there are.
  - caption is the name that will be displayed above your toc
  - glob will read all files specified and automatically create a menu. Use asterisks to match multiple files.

References:
  - Sphinx and Read the Docs: https://docs.readthedocs.io/en/latest/intro/getting-started-with-sphinx.html
  - toctree: https://docs.typo3.org/typo3cms/HowToDocument/WritingReST/MenuHierarchy.html
  - restructuredText: https://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html

Sample **docs** Folder Hierarchy
--------------------------------
This repo uses below folder hierarchy to provide an example structure for your guide. You can modify as needed. 
Reference: https://sphinx-rtd-tutorial.readthedocs.io/en/latest/folders.html 

- class1: F5 ADC
       - module1: Onboarding
             - lab1: Provisioning
             - lab2: setup wizard
       - module2: Configuration Deployment
             - lab1: profiles
             - lab2: pool and pool members
             - lab3: virtual server
       - module3: Troubleshooting
             - lab1: qkview
             - lab2: logs
- class2: F5 Security
- class3: F5 Automation and Orchestration

Other files and folder in this **doc** directory:
------------------------------------

docs > **conf.py** 
~~~~~~~~~~~~~~~~~~
Python configuration file used by Sphinx (documentation tool). Make below arguments to customize this file.

- classname (line 8): This is the name of your lab, used in multiple areas like when creating a pdf
- github_repo (line 11): The location of your github repo, used for the rst_prolog
      
      - https://www.sphinx-doc.org/en/master/usage/configuration. 

- github_url (line 76): The location of your github repo, displayed as the "Edit on GitHub" hyperlink in the html body
- project (line 154): This is the name of the project, used when printing pdf or epub
- htmlhelp_basename (line 229): Output file base name for HTML help builder.

docs > **Makefile** and **make.bat**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Used to set variables that define the location relevant files. Modify below arguments to customize this file.

- SPHINXPROJ: You can change to the name of your project

docs > **preamble.tex**
~~~~~~~~~~~~~~~~~~~~~~~
Used to define the look and feel of the pdf version of your document. Used by LaTex. No modification needed

docs > **_static**
~~~~~~~~~~~~~~~~~~
Folder that stores static graphics and css files for your theme

docs > **_templates**
~~~~~~~~~~~~~~~~~~~~~
Folder that stores files that can be used to overwrite theme files for more customizability.
Current contents use the `F5 clouddocs <https://clouddocs.f5.com/>`__ theme.

docs > **class1**
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

   class*/class*
   module*/module*
