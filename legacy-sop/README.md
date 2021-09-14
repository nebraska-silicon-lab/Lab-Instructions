SOP for CMS Forwardpixel Phase-I manufacturing at UNL
=====================================================

This repository holds the standard operating procedures (SOP) for use in the silcon lab at University of Nebraska-Lincoln. Feel free to use them at other sites as well.

Instructions to create documents
--------------------------------

The SOP documents are written in LaTeX. You will need a current LaTeX distro to make those files. A `Makefile' is procided at your convenience.

If everything is properly set up, do

```
make -j4
````
and the pdf files should appear shortly.

If you like to clean up things after making the pdf's, issue
```
make clean
```
This will delete all intermediate files but keeps the pdf's.

Images
------
The images are either plain jpg (for photos) or png (for drawings). In some cases the source files are present as well. Most of the drawings were made using Inkscape, which allows for a PDF export.

Documentation templates
-----------------------
Some SOP come with a txt-file, which should be used to document the work done using that SOP. Use them as a template in an editor of your choice and upload it to the elog.

Signed-off documents
--------------------
The signed-off versions of the SOP are available [in DocDB](https://cms-docdb.cern.ch/cgi-bin/DocDB/ShowDocument?docid=12623). Annotated links are [on a on a TWiki](https://twiki.cern.ch/twiki/bin/view/CMS/UNLPixelPhaseI "TWiki page hosted at Cern").

