=======================
PRADIOSS Документация
=======================

Documentation is published on `<https://docs.pradis.laduga.com>`_.
To edit it yourself, you need to tinker a bit with Git and Sphinx.
See the `Style Guide` for formatting and style conventions.


License
-------

All documentation in this repository is licensed under the Creative Commons
Attribution 3.0 Unported license (`CC BY 3.0`_).

.. _CC BY 3.0: https://creativecommons.org/licenses/by/3.0/deed.en_US

Style
-----

Source files are written using the `Sphinx Documentation Generator
<https://www.sphinx-doc.org/en/master/>`_. The syntax follows the `reStructuredText
<http://docutils.sourceforge.net/rst.html>`_ style, and can also be edited
from GitHub.


Building
--------

1. Install `pipenv` - https://pipenv.readthedocs.io/en/latest/
2. Create a Python environment (typically inside this repository): `pipenv --python 3.8`
3. Change into the environment: `pipenv shell`
4. Install the dependencies `pip install -r requirements.txt`
5. Now you can use `make ...` to build all the stuff - for example `make html` to build the HTML flavor of all manuals

To change into this environment you need to run `pipenv shell` to launch the shell and to exit you can use either `exit` or `Ctrl` + `D`.

When editing the documentation installing `sphinx-autobuild` though pip can be helpful. This will watch file changes and automatically reload the html preview:

1. Install `pip install sphinx-autobuild`
2. Enter the documentation section `cd user_manual`
3. Watch for file changes `make SPHINXBUILD=sphinx-autobuild html`
4. Open http://127.0.0.1:8000 in the browser and start editing

Icons
-----

To compile and update the icons list in the designer manual, you will also need

1. inkscape
2. sass
3. unzip
4. wget

.. _CC BY 3.0: https://creativecommons.org/licenses/by/3.0/deed.en_US
.. _`Xcode command line tools`: https://stackoverflow.com/questions/9329243/xcode-install-command-line-tools
