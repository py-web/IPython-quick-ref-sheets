####For Ubuntu 12.04 Users.

Download these files and run:

sudo sh Quick_install.sh *-- see Update*

It will install a bunch of packages that are often used in IPython and create
three shortcuts on your desktop.  You may want to edit the path in the IPython 
shorcuts to reflect the directory you want to store your notebooks in. 
Additionally, you will have to manually change the appearance of the icons of 
the shortcuts.  This is done by right clicking on the icon->properties->click on 
the current icon and slect a new one.  Two icons images are among the files 
here.

(Still needs work buts gets most of the big stuff.)

####New Stuff:

The files:

* IPython_dir.py
* IPython3_dir.py

Will open up file dialog boxes which you can use to open IPython in a particular 
directory.  However you still need to use Stop IPython Notebook.sh when you are
done to close all of the IPython processes.

####Update: 

Quick_install.sh is now out of date with the release of IPython 1.1 but a lot of
the packages it installs still need to be installed.  My current procedure uses 
the following apt-get commands.  I am not sure all are necessary and some might 
be missing...

    sudo add-apt-repository ppa:fkrull/deadsnakes
    sudo apt-get update
    sudo apt-get install python-software-properties
    sudo apt-get install python3.3
    sudo apt-get install pandoc g++
    sudo apt-get install python-pip python-zmq python-jinja2 python-pygments
    sudo pip install tornado

    sudo pip install sphinx # to get the latest version of sphinx for nbconvert

    sudo apt-get install curl python3-zmq python3-jinja2 python3-pygments python3-sphinx python3-setuptools

    sudo cp /usr/local/bin/pip /usr/local/bin/pip-2.7 # needed to not lose pip-2.7

    curl -O https://raw.github.com/pypa/pip/master/contrib/get-pip.py
    sudo python3.2 get-pip.py
    sudo pip-3.2 install tornado
    sudo pip-3.2 install sympy # optional for using sympy
    sudo pip-3.2 install matplotlib # optional for plotting
    sudo pip-2.7 install matplotlib # optional for plotting

I also downloaded the IPython source files and installed it with the two following commands:

    sudo python setup.py install
    sudo python3 setup.py install

However I guess I could have used these instead:

    sudo pip-2.7 install ipython
    sudo pip-3.2 install ipython # might not have installed IPython for Python3.3

I'm also not sure if these would have installed the IPython Notebook.