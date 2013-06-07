IPython-quick-ref-sheets
========================

This is ongoing work developing quick reference sheets for IPython.  It is an
attempt to make several versions of the %quickref IPython magic output for ease
of access.

The final goal is to have versions that include .png, .html, and .pdf formats.

Image Files
========================

The current png image files can be seen together [here](http://imgur.com/a/gt0jx#0).

![ScreenShot](https://github.com/damontallen/IPython-quick-ref-sheets/raw/master/Basic_Help.png)

HTML Help Tables
========================

These HTML versions of the quick reference tables were generated in the IPython 
notebook. They render correctly in Chrome, but they to not in
Firefox.  Despite this problem, for now, these HTML files could be modified by someone with
more experience to make them a good reference.

PDF Files
========================

The pdf versions were generated by printing out the HTML rendering from within 
Chrome.  Unfortunately, during the print process the color for the title and the 
headers was removed from the pdfs.  In the future I would like to automate this conversion from within 
the IPython notebook, or just Python with the aid of a HTML to pdf library.


Notebook
========================

The IPython notebook that generated the HTML files can be viewed [here](http://nbviewer.ipython.org/urls/github.com/damontallen/IPython-quick-ref-sheets/raw/master/Qick_ref_with_library.ipynb). It 
first takes the quickref text and converts it to a dictionary with labels for the
title, headings, and comment lines, as well as the multiline examples.  A copy of
the dictionary is saved as a binary pickle and can be downloaded from this git.
The notebook goes on the generate HTML representations of the quickref text.

Quick Referance Text
========================

The text file that this work is based on was generated fromthe IPython source code.  This
was done by downloading a copy of the source code from [here](https://github.com/ipython/ipython/downloads) and inserting the modification 
the "modification_code.py" code into the "basic.py" file.  It was inserted around line 380 to be able to 
add the %quickref_file magic command.  Ideally in the future this command will generate all 
the quick reference file versions.


