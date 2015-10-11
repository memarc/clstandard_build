Currell Berry, 10/11/2015
=================================

This folder contains the tex sources of the final common lisp standard draft, along with a bat script which I have written which compile the standard into a single pdf.  This is the pdf which I make available for download on my site.

The code as written works on windows.  You will have to port makestandard.bat to bash if you want to run on Mac or Linux.

Dependencies
=================================
- pdftex (available as pdftex on PATH)
- ghostscript (available as gswin64c on PATH)

Reproduce
=================================
Below are instructions for how to reproduce the output pdf from scratch, downloading all tex sources from the original source. 

1. Download tex sources for revision dpans3 and dpans3r from http://www.cs.cmu.edu/afs/cs/Web/Groups/AI/lang/lisp/doc/standard/ansi/dpans/ .

2. Copy the dpans3r files into the dpans3 folder, choosing to "overwrite" the conflicts.

3. In chap-0.tex, change the references to ".tc" files to ".toc".  It appears that this change was made upstream between dpans3 and dpans3r, but was not updated in the downloadable sources because dpans3r was not supposed to change any of the actual content files.

4. Copy my script "buildstandard.bat" into the folder, and run it.  It will run pdftex on each chapter in turn, and then combine all the pdfs together using ghostscript. 
