================================================
robotframework-excellibrary for Robot Framework
================================================


Introduction
============

Robotframework-excellibrary is a Robot Framework Library that provides keywords to allow opening, reading, writing and saving Excel files (xls). 
The robotframework-excellibrary leverages two other python libraries xlutils_ and natsort_. Xlutils installs xlrd_ that reads data from an Excel file and xlwt_ write to an Excel file.

.. _xlutils: https://xlutils.readthedocs.io/en/latest/
.. _natsort: https://natsort.readthedocs.io/en/8.1.0/
.. _xlrd: https://xlrd.readthedocs.io/en/latest/
.. _xlwt: https://xlwt.readthedocs.io/en/latest/

- Information about robotframework-excellibrary keywords can be found on the `ExcelLibrary-Keyword Documentation`_ page.
- Information about working with Excel files in Python can be found on the `Python Excel`_ page.
- Useful pdf for practical use with Excel files here_.

.. _`ExcelLibrary-Keyword Documentation`: http://navinet.github.io/robotframework-excellibrary/ExcelLibrary-KeywordDocumentation.html
.. _`Python Excel`: http://www.python-excel.org/
.. _here: http://www.simplistix.co.uk/presentations/python-excel.pdf


Requirements
============
* Python 3.7.x (Newer versions not tested)


Installation
============
Using pip
------------

The recommended installation tool is pip_.

.. _pip: http://pip-installer.org

Install pip.
Enter the following:

    pip install robotframework-excellibrary

Append ``--upgrade`` to update both the library and all 
its dependencies to the latest version:

    pip install --upgrade robotframework-excellibrary

To install a specific version enter:

    pip install robotframework-excellibrary==(DesiredVersion)

Manual Installation
-------------------

To install robotframework-excellibrary manually, install all dependency libraries before installing robotframework-excellibrary.

#. Download source distributions (``*.tar.gz``) from here_.
#. Open command line:

       pip install <tar.gz path>

Uninstall
=========

To uninstall robotframework-excellibrary use the following pip command: 

    pip uninstall robotframework-excellibrary

Directory Layout
================

*ExcelLibrary/ExcelLibrary.py* :
    The Robot Python Library that makes use of the xlutils and natsort.

*Tests/acceptance/ExcelRobotTest.robot* :
    Example test file to display what various keywords from robotframework-excellibrary accomplish

*doc/ExcelLibrary-KeywordDocumentation.html* :
    Keyword documentation for the robotframework-excellibrary.


Usage
=====

To write tests with Robot Framework and robotframework-excellibrary, 
ExcelLibrary must be imported into your Robot test suite.
See *doc/ExcelLibrary-KeywordDocumentation.html* for more information.


Running the Demo
================

The test file ``ExcelRobotTest.robot``, is an easily executable test for Robot Framework using robotframework-excellibrary. 
For in depth detail on how the keywords function, read the `Keyword documentation`_.

.. _`Keyword documentation`: http://navinet.github.io/robotframework-excellibrary/ExcelLibrary-KeywordDocumentation.html

To run the test, open a command prompt within the *Tests/acceptance* folder and run:

    robot ExcelRobotTest.robot


Things to Note When Using robotframework-excellibrary
=====================================================

* When using the keyword *Add New Sheet* the user cannot perform any functions before or after this keyword on the currently open workbook. The changes that other
  keywords make will not be saved when the keyword *Add New Sheet* is used. They must add a sheet then save the workbook before using any other keyword.
  If they want to use any other keywords on the workbbok they must open the workbook again to do so.
* We cannot use xlsx files as this has not been implemented in the xlrd library. To get round this issue, consider using `robotframework-excellib`_.

.. _`robotframework-excellib`: https://pypi.org/project/robotframework-excellib/


Getting Help
============
The `user group for Robot Framework`_ is the best place to get help. Include in the post:

- Contact the `Python-Excel google group`_
- Full description of what you are trying to do and expected outcome
- Version number of robotframework-excellibrary and Robot Framework
- Traceback or other debug output containing error information

.. _`user group for Robot Framework`: http://groups.google.com/group/robotframework-users
.. _`Python-Excel google group`: https://groups.google.com/forum/#!forum/python-excel