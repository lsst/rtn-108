.. image:: https://img.shields.io/badge/rtn--108-lsst.io-brightgreen.svg
   :target: https://rtn-108.lsst.io
.. image:: https://github.com/lsst/rtn-108/workflows/CI/badge.svg
   :target: https://github.com/lsst/rtn-108/actions/

################################
CCD Height Effects on Rubin PSFs
################################

RTN-108
=======

Modeling the point-spread function (PSF) precisely is essential for many-- if not all-- science cases with the Rubin Observatory. In this work, we inspect a PSF residual pattern present in both Rubin's ComCam and LSSTCam observations. We show that it is likely due to effects from CCD non-flatness, and elaborate on the mechanism by which height offsets could influence the PSF. Finally, we demonstrate that incorporating height information into PSF modeling greatly reduces the observed residual.

Links
=====

- Live drafts: https://rtn-108.lsst.io
- GitHub: https://github.com/lsst/rtn-108

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst/rtn-108

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the ``acronyms.tex`` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf
