c-test project
==============

|Travis| |Codacy Badge| |Coveralls| |Documentation Status|

Installation
------------

Use ``brew`` and not ``apt`` if you are on macos!

.. code:: bash

   $ sudo apt install cmake gcc lcov cppcheck python-pip valgrind flawfinder doxygen dot
   $ git clone https://github.com/chdemko/c-test.git
   $ [sudo] pip install [--user] -r c-test/docs/requirements.txt

Usage
-----

Compilation
~~~~~~~~~~~

.. code:: bash

   $ mkdir build
   $ cd build
   $ cmake ../c-test -DBUILD_COVERAGE=1 -DBUILD_HTML_COVERAGE=1 -DUSE_VALGRIND=1 -DRUN_CPPCHECK=1
   $ make

Run test and code coverage
~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code:: bash

   $ make test
   $ make coverage
   $ make html-coverage

Check style
~~~~~~~~~~~

.. code:: bash

   $ make cclint

Run flaw finder
~~~~~~~~~~~~~~~

.. code:: bash

   $ make flawfinder

Build the docs
~~~~~~~~~~~~~~

.. code:: bash

   $ make docs

Create archives
~~~~~~~~~~~~~~~

.. code:: bash

   $ make package
   $ make package_source

Install package
~~~~~~~~~~~~~~~

.. code:: bash

   $ make install

.. |Travis| image:: https://img.shields.io/travis/chdemko/c-test.svg
   :target: http://travis-ci.org/chdemko/c-test
.. |Codacy Badge| image:: https://img.shields.io/codacy/grade/8cd40a98b85f4d4bbea18469cd062bb7.svg
   :target: https://www.codacy.com/app/chdemko/c-test
.. |Coveralls| image:: https://img.shields.io/coveralls/chdemko/c-test.svg
   :target: https://coveralls.io/r/chdemko/c-test?branch=master
.. |Documentation Status| image:: https://img.shields.io/readthedocs/c-test.svg
   :target: http://c-test.readthedocs.io/en/latest/?badge=latest
