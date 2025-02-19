Empty example PYPI package by leecampbellc85
############################################


Change log 
###########

* version 0.0.1.12
    * Basic unittest for Core module
    * Documentation
* version 0.0.1.6
    * Execute this from command-line (pfpy -v)
* version 0.0.0.1
    * Init files and directory structure


Requirements
#############

* Linux OS or Windows OS
* Python (2.7)


Basic install
#############

.. code-block::

    pip install perfect-pypi --upgrade


(install without cache: pip install perfect-pypi --no-cache-dir  )


You can find the detailed documentation in https://github.com/leecampbellc85/perfect-pypi.


Usage
######

From command line
**********************

* Usage:
    * pfpy --version
    * pfpy core --input TEXT
    * pfpy core -i TEXT -o string
    * pfpy core -i TEXT --output json
* Arguments:
* Options:
    * **-h** **--help**        show this help message and exit
    * **-v --version**         show version and exit
    * **--verbose**            print status messages
    * **-i --input**           set input and exit
    * **-o --output**          output format default is string. Possible values: string, json

You merely type the **pfpy** command to commandline with the required parameters.
* *pfpy --version* or *pfpy -v* : Get version of our package
* *pfpy core --input TEXT * or *pfpy core -i TEXT -o string* : Write out to screen the TEXT in string format. (module: core)
* ``` pfpy core -i TEXT --output json ``` : Write out to screen the TEXT in json format. (module: core)

From Python
*************************

Import the required module from perfectpypi package in python

.. code-block::

    import perfectpypi


Examples
########

From command line
**************************

1. Get version:
"""""""""""""""""""""

.. code-block::

    pfpy -v


Result: 
.. code-block::

    0.0.1.11



2. Write out text in string format:
""""""""""""""""""""""""""""""""""""""""

.. code-block::

    pfpy core -i "Hello World"

Result: 

.. code-block::

    Hello World



3. Write out text in json format:
"""""""""""""""""""""""""""""""""""""""""

.. code-block::
    
    pfpy core -i "Hello World" -o json


Result: 

.. code-block::
    
    [{'text': 'Hello World'}]



From Python
*********************

Every example assumes you are in python shell

1. Execute core module related unittest
""""""""""""""""""""""""""""""""""""""""""""""""""

.. code-block::

    from perfectpypi.core.perfectpypi_core_unittest import *
    testResult = runUnittests()


Result:

.. code-block::

    test_input (perfectpypi.core.perfectpypi_core_unittest.TestCoreModule) ... All tests passed so far!
    ok
    test_output (perfectpypi.core.perfectpypi_core_unittest.TestCoreModule) ... All tests passed so far!
    ok

    ----------------------------------------------------------------------
    Ran 2 tests in 0.003s

    OK


2. Write out text in string format:
""""""""""""""""""""""""""""""""""""""""""""""""""

.. code-block::

    from perfectpypi.core.perfectpypi_core import *
    getText("Hello World")


Result: 

.. code-block::

    Hello World



3. Write out text in json format:
""""""""""""""""""""""""""""""""""""""""""""""""""

.. code-block::

    from perfectpypi.core.perfectpypi_core import *
    getText("Hello World", "json")

Result: 

.. code-block::

    {'text': 'Hello World'}



Known issues
#############


**Permission denied on /usr/bin/pfpy**
*******************************************

Sometimes you are facing the following issue when you execute the **pfpy** command:

.. code-block::
    
    -bash: /usr/bin/pfpy: Permission denied


Solution to execute the following command:

.. code-block::

    sudo chmod +x /usr/bin/pfpy


**Command not found on /usr/bin/pfpy**
*******************************************
Although the package is well prepared sometimes you are facing the following issue after a package update when you execute the **pfpy** command:

.. code-block::

    /usr/bin/pfpy: line 2: $'\r': command not found
    /usr/bin/pfpy: line 19: syntax error: unexpected end of file


Solution to execute the following command:

.. code-block::

    sudo dos2unix /usr/bin/pfpy



LICENSE (MIT)
#############


Copyright (c) 2019

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do
so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
