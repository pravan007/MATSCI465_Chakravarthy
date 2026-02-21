# MATSCI465_Chakravarthy

This repository was created for _Assignment 1_ of **MAT_SCI 465** _Advanced Electron Microscopy_. Also created for this assignment was an environment **matsci465**, on which the following packages were installed: Jupyter, NumPy, SciPy, Matplotlib, Scikit-Learn, HyperSpy, py4DSTEM, OpenCV.

As of 1/12/2026, this repository contains this _README_ file, an _environment.yml_ file, and the notebook _assignment_01_setup.ipynb_, which contains some environment/OS verification steps as well as a cursory analysis of an EM image.

**Assignment 02 Update, 2/6/2026**

This repository now contains a 4D-STEM analysis pipeline, in _assignment_02.ipynb_, as well as two resulting images (_Virtual_BF.png_, _Virtual_ADF.png_).

Virtual detectors allow "replaying" of an experiment by integrating certain pixels of an experimentally generated image and ignoring others. This allows for the creation of bright- or dark-field images that enhance resolution and make visualization easier, according to the geometry of the chosen virtual detector. For example, a bright field detector only collects pixels within an inner disk, while an annular dark field detector only collects pixels within a ring around a central disk. Using virtual detectors in this manner is possible in 4D-STEM because the diffraction pattern is collected throughout the entire sample, rather than in specific regions.

**Assignment 03/04 Update, 2/20/2026**

This assignment developed a variety of classical, machine learning, and deep learning techniques for image analysis using about 200 images from the DOPAD dataset. The methods are as follows:

*Watershed algorithm:* A classical segmentation method that treats image space topographically, determining particle boundaries by prioritizing the identification of points of lowest intensity. It is the fastest of the methods used here, and is useful for cursory morphological scans or datasets with gradient-based objects.

*SVM & Random Forest:* Support Vector Machines and Random Forest are two supervised machine learning techniques for image classification. SVM attempts to find maximal separations between data points, while Random Forest uses an aggregation of decision trees on different subsets of the data. Though both models' F1 scores were high, I found the Random Forest score to be higher (0.998 vs 1.0). Neither model was time- or compute-intensive, making either of them (but more so Random Forest) a useful all-around solution.

*K-Means clustering:* An unsupervised machine learning method that iteratively groups together clusters of data for classification. While not the fastest, this technique can be deployed along with principal component analysis (PCA) to more straightforwardly visualize data trends. Compared to Random Forest, the k-means model is less precise but more transparent. Testing a few values for *k* (number of clusters), I found *k*=3 to have the best silhouette score (0.279).

*CNN & U-Net:* A convolutional neural network (CNN) is a deep learning architecture using hierarchically connected layers to classify and segment image features. U-Net is a segmentation-specific type of CNN with a U-shaped architecture consisting of encoder and decoder portions joined by skip connections. These two architectures allow large-scale automation of feature detection, while also working well without labeled data (U-Net especially). I will update this document when I finish debugging these sections.
