# DUNE Technical Proposal (TP)
Info and links on this page:

* Guidelines
* Quick Start
* Best Practices
* Find auto-build PDF files of each Volume
* Management
* Major news (regarding any changes to this repository)

## Guidelines and information

Please follow the editing guidelines in [Document Guidance](https://github.com/DUNE/document-guidance). You will find information on:
* how to use git
* how to get the files and build the document
* DUNE standards for editing (images, tables, labels, citations, numbers/units, upper/lower case, grammar, punctuation, inserting "fixmes", etc.)

A Quick Start section from the guidance document web page is copied below
Do you want to reference content from the CDR? Go to [CDR](https://github.com/DUNE/cdr).


## Quick start
This shows how to clone the TDR repository and build the physics volume. Bare bones. See more detailed and non-TDR-specific information in the "Best practices" and "Getting Started" sections below.

-  [[https://help.github.com/articles/signing-up-for-a-new-github-account][Get a github account]] and send your username to Brett (see bottom of page).
-  [[https://github.com/DUNE/document-guidance/blob/master/install-git-on-mac.org][Install Git on Mac]], requires Mac OS X, [[https://appleid.apple.com][Apple ID]], [[https://developer.apple.com/xcode/downloads][XCode]], and [[https://developer.apple.com/download/more/][Command Line Tools]].
-  [[https://desktop.github.com/][Github Desktop]] Manage your [[https://guides.github.com/introduction/flow/][GitHub flow]] using this dandy interface. 

If you need a reliable LaTeX installation, Tom Junk has installed texlive 2017 in his area on the dunegpvm's at Fermilab. Feel free to use it! Just login and run his setup file:

#+BEGIN_EXAMPLE
  $ ssh dunesl7gpvm01.fnal.gov  
  for bash and sh:  $ source /grid/fermiapp/products/dune/texlive2017/setup.sh
  for tcsh and csh: $ source /grid/fermiapp/products/dune/texlive2017/setup.csh
  $ mkdir /my/work/area
#+END_EXAMPLE


 
- Type this sequence to clone the repository:
#+BEGIN_EXAMPLE
  $ cd /my/work/area
  $ git clone https://github.com/DUNE/DUNE-TDR.git
#+END_EXAMPLE
 
- Do a test edit and test build (yes, run pdflatex twice)
#+BEGIN_EXAMPLE
  $ cd DUNE-TDR
  $ pdflatex volume-physics
  $ pdflatex volume-physics
#+END_EXAMPLE
 
- Type this sequence to commit (after it builds successfully):
#+BEGIN_EXAMPLE
  $ git commit -a -m "Brief explanation of what you updated"
  $ git push
#+END_EXAMPLE


## Best practices for interacting with GitHub
Please follow these four important guidelines that will help avoid headaches:

1. *Always do a pull immediately before you begin working on a file just in case someone else modified it recently.*
2. *We recommend that you compile frequently as you compose and edit; it will be easier to resolve any compilation problems.*
3. *Make sure the document compiles before you commit it and push it to the repository. Ask Anne if you need help.*
4. *Commit and push immediately after you finish your edits so that others have the best chance of picking up your changes before they edit.  (Yes, git can resolve conflicts, but it's better to avoid them.)*

## Autobuilt PDFs from the repository

Shortly after successful commits are pushed, these links should point to updated files:  

* [Executive Summary Volume](https://dune.bnl.gov/docs/executive-summary.pdf)
* [FD Single-Phase Volume](https://dune.bnl.gov/docs/far-detector-single-phase.pdf)
* [FD Dual-Phase Volume](https://dune.bnl.gov/docs/far-detector-dual-phase.pdf)
* [Software and Computing Volume](https://dune.bnl.gov/docs/software-computing.pdf)

If a build fails an error message will be sent to the committer.



## Management

* The management area in the DUNE wiki for development of this volume is at [Technical Proposal](https://wiki.dunescience.org/wiki/Technical_Proposal).
* We may also maintain assignments and status info at [Technical Proposal Tracking](https://wiki.dunescience.org/wiki/Technical_Proposal_Tracking).

For general DUNE information: Go to [DUNE at Work](https://web.fnal.gov/collaboration/DUNE/SitePages/home.aspx)


## Major News
Repository created 19 December 2017!

-- Anne Heavey

