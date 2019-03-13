
Build on Linux
==============

Best to build in a Python Virtual Environment

To check/create the venv and use it in the build::

 make -f venv.mk html

The venv.mk will create/update a virt env (if not availablie ) in current dir/venv AND run the html build in it.

If you want for some reason start from scratch::

 make -f venv.mk cleanall

You can also use that virtual environment later doing::

 source/bin/activate

to activate the venv and then run the build from within that venv::

 make html

Alternive
.........

You can also use your own virtual env by creating it using it first::

 # you NEED python >3.6. Depending on distro either use `python3` or `python`
 # common name is 'venv' but call it whatever you like

 python3 -m venv venv  # using the venv module, create a venv named 'venv'

Then activate the venv and install the requirements via the REQUIRMENTS.txt::

 cd venv
 source ./venv/bin/activate
 pip install -r REQUIREMENTS.txt

and run the build from within that venv::

 make html


Build on Windows
================

::

 pip install -r REQUIREMENTS.txt venv
 venv/source/bin/activate
 make.bat



