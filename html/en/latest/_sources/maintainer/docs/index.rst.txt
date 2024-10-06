Documentation Developer Guide
=============================

Documentation is managed, built and published using:

* `reStructuredText`_ (RST) content stored in GitHub repositories.  
* `Sphinx`_ documentation generator.
* `Read the Docs Sphinx Theme`_ for styling.
* `Read the Docs`_ for hosting.

When changes are pushed to the git repository this triggers the Read the Docs
build pipeline and the resulting HTML is hosted via their servers. However,
before this is done the site should be generated locally, so as to verify
formatting and avoid continually pushing, having to wait for the site to build
and risking errors going live. Only when the local build looks good do we commit
and push.

RST content is located alongside project materials — e.g. software sources and
PCB design databases — in the same git repository. This has a number of
benefits:

* The same workflow with branching and pull requests etc. can be used to manage
  contributions.
* Sphinx can auto-document Python code and via plugins, other programming
  languages that are supported by Doxygen.
* Project materials + documentation are managed and tagged together.

Obviously projects such as this one that are purely documentation, will have
only the Sphinx config and content in their repo.

To find out where the source RST for a page is located, click on the Edit on
GitHub link top-right to locate the GitHub repository containing this.

.. toctree::
   :maxdepth: 1
   :hidden:

   tooling
   formatting

.. _reStructuredText: https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html
.. _Sphinx: https://www.sphinx-doc.org
.. _Read the Docs Sphinx theme: https://sphinx-rtd-theme.readthedocs.io/en/stable/
.. _Read the Docs: https://readthedocs.com