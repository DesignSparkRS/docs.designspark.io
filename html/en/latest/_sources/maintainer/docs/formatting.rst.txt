Formatting
==========

General
-------

For general notes on reStructuredText (RST) formatting see:

* `Introduction to reStructuredText <https://www.writethedocs.org/guide/writing/reStructuredText/>`_
* `reStructuredText Primer <https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html>`_

There are various editors available with RST support, such as Visual Studio Code with the `reStructuredText plugin <https://marketplace.visualstudio.com/items?itemName=lextudio.restructuredtext>`_.

Notes on less obvious formatting methods are provided below.

Linking to other project documentation
--------------------------------------

While it's possible to link to the documentation for another project just as you
would a regular website, it's better to use Intersphinx where this is also 
Sphinx-based. Benefits include that you can then use a shorter cross-reference 
role each time, rather than a full URL, as well there being just one place to 
update the mapping should the host or URL path on the server change. For details, 
see:

https://docs.readthedocs.io/en/stable/guides/intersphinx.html

If the target Sphinx project has not previously been linked to, it will likely be
neccessary to update :code:`conf.py` in the project you would like to link from,
in order to add a new Intersphinx mapping.

Subscript and Superscript
-------------------------

Subscript and superscript characters can be generated using the ``:sub:`` and
``:sup:`` roles. For example:

.. code-block:: rest

    Upper limit 10\ :sup:`6`. See note\ :sub:`2`.

Gives:

Upper limit 10\ :sup:`6`. See note\ :sub:`2`.

.. note::
   Interpreted text needs to be surrounded by whitespace or punctuation, which
   means that if we don't want a gap, e.g. between ``10`` and ``6``, or between
   ``note`` and ``2``, we need to escape the whitespace with a backslash.

Non-ASCII Characters
--------------------

Non-ASCII characters can be inserted by using substitutions and these are
defined in the file ``substitutions.txt`` in the root of the Sphinx project.
For example, the right arrow (|rarr|) is inserted by entering ``|rarr|``.  If a
character is not currently supported, simply look up the Unicode ID and add it
to substitutions.txt.