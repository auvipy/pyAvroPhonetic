==============
pyAvroPhonetic
==============

A Python implementation of the popular Bengali phonetic-typing software
`Avro Phonetic`_.

Branch: Master: |Master| | Develop: |Develop|

Overview
========

pyAvroPhonetic provides a Python package which includes a text parser
that converts Bangla written in Roman script to its phonetic
equivalent in Bangla. It implements the *Avro Phonetic Dictionary
Search Library* by `Mehdi Hasan Khan`_.

Currently supported and tested Python versions are 2.7 and
3.5.

*N.B. This package is under development and is not yet fit for
production use.*

Inspirations
------------

This package is inspired from `Rifat Nabi`_\'s `jsAvroPhonetic`_. So
far, the code is a direct (and shameless) translation of
jsAvroPhonetic into Python.

Installation
============

With Pip
--------

**Option 1. Using Pip (the easy way) (recommended):**

::

    $ sudo pip install PyAvroPhonetic

**Option 2. Using Pip in a Virtualenv (needs virtualenv):**

::

    $ virtualenv pyAvroPhonetic
    $ cd pyAvroPhonetic
    $ source bin/activate
    $ pip install PyAvroPhonetic

Without Pip
-----------

**Option 3. Using Git (needs git):**

::

    $ git clone https://github.com/kaustavdm/pyAvroPhonetic
    $ cd pyAvroPhonetic
    $ sudo python setup.py install

**Option 4. Using Git in a Virtualenv (needs git and virtualenv):**

::

    $ virtualenv pyAvroPhonetic
    $ cd pyAvroPhonetic
    $ source bin/activate
    $ git clone https://github.com/kaustavdm/pyAvroPhonetic
    $ cd pyAvroPhonetic
    $ python setup.py install

Usage
=====

At present, only the text parser has been implemented. It can be accessed as:

::

    >>> from pyavrophonetic import avro
    >>> avro.parse('aami banglay gaan gai')

Contributing
============

**Fork** -> **Do your changes** -> **Send a Pull Request**. It's that
easy!

Note for developers
-------------------

Coding style follows `PEP 8`_ along with `PEP 257`_ for Docstring
conventions. Unit tests are run using the Nose library and syntax and style
checking is done with Pylint.

Please install these two libraries in your development
environment. The `tests/requirements.txt` file specifies testing
dependencies. To install them with `pip`:

::

    $ sudo pip install -r tests/requirements.txt

Pylint is used with some modifications
to the default configuration. The notable ones are:

 - W0142 is ignored to allow usage of "magic methods"
 - Maximum branches in function body: 20
 - Maximum statements in function body: 100

For others please see the [Design] section in pylint-rc.ini. Our
target is to keep up a score of *10.0/10* in Pylint's reports. Tests
on Travis will fail if Pylint doesn't give 10.0/10. This is
intentationally used to ensure uniform code structure and quality.

Run unit tests from the root of the repository:

::

    $ nosetests --exe -v

Run pylint from root of the repository:

::

    $ pylint --rcfile=pylint-rc.ini pyavrophonetic

We need more testers
--------------------

If you find any bugs, please report them in the Issues queue. As
always, before you report any new issue, please check that it has not
been already posted by someone else.

Acknowledgements
================

 - Mehdi Hasan Khan for originally developing and maintaining Avro
   Phonetic
 - Rifat Nabi for porting it to Javascript
 - `Md Enzam Hossain`_ for helping me understand the ins and outs of
   the Avro dictionary and the way it works
 - `Sarim Khan`_ for writing ibus-avro which helped to clarify my
   concepts further
 - `Asif Saif Uddin`_ for takeover of the current maintainership role. 

License
=======

Copyright (C) 2024 Asif Saif Uddin <auvipy@gmail.com>.

::

    This file is part of pyAvroPhonetic.

    pyAvroPhonetic is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    pyAvroPhonetic is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with pyAvroPhonetic.  If not, see <http://www.gnu.org/licenses/>.

The full license text can be found in ``LICENSE``.

.. _Avro Phonetic: http://omicronlab.com
.. _Mehdi Hasan Khan: https://github.com/omicronlab
.. _Rifat Nabi: https://github.com/torifat
.. _jsAvroPhonetic: https://github.com/torifat/jsAvroPhonetic
.. _PEP 8: http://www.python.org/dev/peps/pep-0008/
.. _PEP 257: http://www.python.org/dev/peps/pep-0257/
.. |Master| image:: https://travis-ci.org/TrendBreaker/pyAvroPhonetic.png?branch=master
   :target: https://travis-ci.org/TrendBreaker/pyAvroPhonetic
.. |Develop| image:: https://travis-ci.org/TrendBreaker/pyAvroPhonetic.png?branch=develop
   :target: https://travis-ci.org/TrendBreaker/pyAvroPhonetic
.. _Md Enzam Hossain: https://github.com/ienzam
.. _Sarim Khan: https://github.com/sarim
