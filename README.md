# MATSCI465_Chakravarthy

This repository was created for _Assignment 1_ of **MAT_SCI 465** _Advanced Electron Microscopy_. Also created for this assignment was an environment **matsci465**, on which the following packages were installed: Jupyter, NumPy, SciPy, Matplotlib, Scikit-Learn, HyperSpy, py4DSTEM, OpenCV.

As of 1/12/2026, this repository contains this _README_ file, an _environment.yml_ file, and the notebook _assignment_01_setup.ipynb_, which contains some environment/OS verification steps as well as a cursory analysis of an EM image.

**Assignment 02 Update, 2/6/2026**

This repository now contains a 4D-STEM analysis pipeline, in _assignment_02.ipynb_, as well as two resulting images (_Virtual_BF.png_, _Virtual_ADF.png_).

Virtual detectors allow "replaying" of an experiment by integrating certain pixels of an experimentally generated image and ignoring others. This allows for the creation of bright- or dark-field images that enhance resolution and make visualization easier, according to the geometry of the chosen virtual detector. For example, a bright field detector only collects pixels within an inner disk, while an annular dark field detector only collects pixels within a ring around a central disk. Using virtual detectors in this manner is possible in 4D-STEM because the diffraction pattern is collected throughout the entire sample, rather than in specific regions.
