IPython-quick-ref-sheets
========================

This project represents ongoing work developing quick reference sheets for IPython.  It is an
attempt to make several versions of the %quickref IPython magic output for ease
of access.

The final goal is to have versions that include .png, .html, .svg, and .pdf formats.

SVG Images
========================

###Basic Commands

![Basic help](http://damontallen.github.io/IPython-quick-ref-sheets/svg/Basic_Help.svg)

###Magic Commands
![Magic help](http://damontallen.github.io/IPython-quick-ref-sheets/svg/Magic_only.svg)

The IPython Notebook used to develop the SVG images is [here](http://nbviewer.ipython.org/urls/raw.github.com/damontallen/IPython-quick-ref-sheets/master/SVG_Table_Builder.ipynb).  It contains a custom magic command to grab the text of the %quickref magic command.
However, the libraries that the notebook references are only in this git page.

(FYI The SVG files above are also available for downloading on [this github.io page](http://damontallen.github.io/IPython-quick-ref-sheets/).)

Image Files
========================

These image files are from screenshots for the HTML version of the quick reference tables.

![ScreenShot](https://github.com/damontallen/IPython-quick-ref-sheets/raw/master/Basic_Help.png)
![ScreenShot2](https://github.com/damontallen/IPython-quick-ref-sheets/raw/master/Magic_only.png)


HTML Help Tables
========================

The HTML versions of the quick reference tables above were generated in the IPython 
notebook. They render correctly in Chrome, but they do not in
Firefox.  Despite this problem, for now, these HTML files could be modified by someone with
more experience to make them a good reference.
(I believe the problem is due to not specifying the font family but I haven't tried the modification yet.)

PDF Files
========================

The pdf versions were generated by printing out the HTML rendering from within 
Chrome.  Unfortunately, during the print process the color for the title and the 
headers was removed from the pdfs.  In the future I would like to automate this conversion from within 
the IPython notebook, or just Python with the aid of a HTML to pdf library.  I have not tried
generating the pdf using the SVG images yet.

Notebook
========================

The IPython notebook that generated the HTML files can be viewed [here](http://nbviewer.ipython.org/urls/github.com/damontallen/IPython-quick-ref-sheets/raw/master/Qick_ref_with_library.ipynb). It 
first takes the %quickref text and converts it to a dictionary with labels for the
title, headings, and comment lines, as well as the multiline examples.  A copy of
the dictionary is saved as a binary pickle and can be downloaded from this git.
The notebook goes on the generate HTML representations of the quickref text.

Quick Reference Text
========================

Originally the text file that this work is based on was generated from the IPython source code.  This
was done by downloading a copy of the source code from [here](https://github.com/ipython/ipython/downloads) and inserting the modification 
the "modification_code.py" code into the "basic.py" file.  It was inserted around line 380 to be able to 
add the %quickref_file magic command.  

Now a custom magic command, added at runtime in an IPython notebook, is used to generate the text.  
Since the magic is now used at run time, the resulting text no longer needs to be saved to a file.
The magic and insertion code is in the [SVG notebook](http://nbviewer.ipython.org/urls/raw.github.com/damontallen/IPython-quick-ref-sheets/master/SVG_Table_Builder.ipynb).


Other Thoughts
========================

[Another aproach](http://ubuntuone.com/6qEHHRVcJKd53TfEEpsCW1) was taken by Thomas Kluyver in which he manually developed
a quick referance sheet using Scribus. It looks better than the standard table currently rendered so in the future I 
would like to switch to that style.  I encourage anyone who wants to make that change, or any other improvements, to do so.
FYI, Inkscape is a open source vector graphics editor that could also be used to edit the SVG images above.

The use of the [webkit](http://www.webkit.org/) library may be a way around using Chrome to generate the png versions.

This [IPython Notebook](http://nbviewer.ipython.org/urls/github.com/damontallen/IPython-quick-ref-sheets/raw/master/SVG_Table_Class-lib%2520test.ipynb) contains experiemntal results building tables from SVG parts.
