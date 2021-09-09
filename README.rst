<<<PROJNAME>>>
==============

This repository stores my contribution to the <<<PROJNAME>>> project.

**This repository is currently private but may be public once a paper is out.**
Documents that should be private (due to copyright or other reasons) are stored in `misho104/<<<PROJNAME>>>-private <https://github.com/misho104/<<<PROJNAME>>>-private>`_ repository.


Copyright
---------

© Sho Iwamoto (and collaborators), 2021

License requirements are contained in the beginning of each file.
If not, the file is not licensed to you.
Contact `me <https://www.misho-web.com/phys/>`_ for further inquiry.

See the following pages for further information on each license.

- `the Creative Commons CC-BY-NC 4.0 International Public License <https://creativecommons.org/licenses/by-nc/4.0/>`_
- `the Apache License, version 2.0 <https://www.apache.org/licenses/LICENSE-2.0>`_
- `CC0 <https://creativecommons.org/publicdomain/zero/1.0/legalcode>`_


Directories
-----------

- **vendor** directory is a special directory, which stores external packages; the usage is described below.
- **notes** directory has my notes; all notes (i.e., TeX documents) should be stored here.



External packages and Vendor directory
--------------------------------------

The codes in this repository depend on various external packages and tools, which are currently categorized as ``pip`` tools and ``submodule`` tools.

If the ``vendor`` directory has ``requirements.txt``, this repository depends on ``pip`` tools for Python codes.
One can install them by ``pip`` command,

.. code-block:: sh

   pip install -r vendor/requirements.txt

Note that this command installs the package to your *system*.
If you are not confident on what you are doing, it may be better to install one-by-one by reading ``requirements.txt``.
Using env-tools such as ``pipenv`` are also recommended, with which you can sequester the Python system for this package from the Python system for the whole machine by so-called virtualenv mechanism (e.g., ``pyenv-virtualenv``). For details, consult Google.

``submodule`` tools are linked to this repository via ``git-submodule`` mechanism, which is invoked by

.. code-block:: sh

   git submodule init
   git submodule update

and then the packages are automatically installed in ``vendor`` directory, after which one should compile those packages one by one.

``vendor/Makefile`` is provided to do the above all at once, but I do not guarantee if ``make`` works in your environment.
Rather, the ``Makefile`` is prepared to inform you which version of tools are used in this analysis and how they are compiled (possibly with patches).

