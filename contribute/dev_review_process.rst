.. OpenCMISS Review Process

==============
Review Process
==============

Check for the Green Tick
========================

Before accepting a tranche of work into the appropriate OpenCMISS prime repository, check that Jenkin's has tested and passed the code.  The status of the code is shown in the last commit of a pushed group of commits in the pull request.  The last commit will have a red cross for a failed build or a green tick for a passed build.  Make sure that the last commit has a green tick before merging.

Check the Documentation
=======================

The documentation for the project is built as part of the testing process.  The details link at the bottom of the pull request web page will take you to the Jenkin's build of the library, this page shows the results of the unit tests for each target operating system, the results of the memory check test, and the results of the documentation build.

.. The Documentation Builder link (entry 2. in step 5.) will take you to the build for the documentation.  On this page you can see the steps taken to build the documentation.  In the last step of the build (step 7.) there is a link 'dox' (entry 2.) that will take you to the built documentation.

The documentation should be reviewed in it's final format particularly those parts of the documentation that (should) have changed due to the current pull request.

Comments Resolved
=================

All comments on the pull request and associated issue should be responded to and satisfied.  It is the reviewers responsibility to check that this has happened before merging the pull request.

Coding Standard
===============

Ensure the code being committed conforms to the standard of code that is expected for OpenCMISS.  See the :doc:`Coding Standards <dev_coding_standard>` document for these guidelines.

Merging
=======

When merging a pull request the reviewer should add a comment so that the corresponding issue is closed.  This can be done by adding a directive to the merge commit, like so::

   closes #2

where the numeral corresponds to the issue that needs to be closed.  You can use other directives that will achieve the same outcome, `here <https://help.github.com/articles/closing-issues-via-commit-messages/>`_ is a list of all directives that will work on GitHub.

