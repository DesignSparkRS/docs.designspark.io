Tooling
=======

Setup
-----

The Python venv module is used to create a virtual environment into which the
Python dependencies are installed. These are specified in requirements.txt,
which is also used by the Read the Docs build pipeline.

To install git and venv on Ubuntu:

.. code-block:: bash

    sudo apt install git python3-venv

This only needs to be done once.

Then if we wanted to edit this documentation, for example:

.. code-block:: bash

    git clone git@github.com:DesignSparkRS/DSDocs.git

    cd DSDocs

    python3 -m venv venv

    source venv/bin/activate

    pip install -r requirements.txt

The above steps need would to be carried out for each project where we want to
edit documentation.

Use 
---

Simply edit the RST content and then to build locally:

.. code-block:: bash

   make html

Following which the generated HTML can be found in the :code:`_build` directory.

With project repositories that contain documentation and other outputs, such as
software sources or gateware etc., please prefix the git commit message with
"Docs: " so that it is clear that the commit pertains to documentation only.

.. note::
   1. With every new terminal it will be neccessary to source the script
      :code:`venv/bin/activate` in order to activate the Python virtual environment.
   2. The pip install command may need to be run from time to time, e.g. after
      a dependency has been updated or a new one has been configured.
   3. If your Python virtual environment somehow gets in a mess, just delete it,
      re-initialise and pip install the dependencies again.

.. warning::
   Do not attempt to commit the contents of the venv directory, as we don't want
   this to be pushed to GitHub. This usually shouldn't be possible, as the venv
   directory should be listed in .gitignore for all projects, but it's worth 
   noting this here also just in case!

.. _reStructuredText: https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html
.. _Sphinx: https://www.sphinx-doc.org
.. _Read the Docs Sphinx theme: https://sphinx-rtd-theme.readthedocs.io/en/stable/
.. _Read the Docs: https://readthedocs.com
