# python-callada-template
Python call Ada template

This is a simple demo project that shows the principles of integration
between Ada and Python (here: Python program calling Ada module).

In order to compile this project execute:

$ gnatmake -Pada_module

As a result a simple loadable library will be created in the ./lib directory
that can be loaded from the Python interpreter in order to extend it
with new functionality. This module is loaded by a test Python script.

To run the script execute:

$ python python_main.py

Note that the Python script uses the ctypes facility, which allows to
dynamically describe the loaded library - the initial section of the Python
script is necessary to describe the functions that will be used later.
This section will be naturally bigger with more complex modules and
the recommended approach is to prepare a separate Python wrapper for that.
This was not done in this demo for simplicity.

REF: http://www.inspirel.com/

