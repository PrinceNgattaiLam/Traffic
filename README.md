# TRAFIC - TRACTS FIBERS CLASSIFICATION USING DEEP LEARNING

## What is it ?
Trafic is a program that performs classification of tract fibers using deep learning algorithms. This extension uses ITK and VTK Libraries to extract features from the fibers, and Tensorflow, for all the deep learning part, meaning the training and the testing.

## Requirements

### Packages
* ITK (v4.7 and above)
* VTK (v6.1.0 and above)
* SlicerExecutionModel
### Software
* Slicer with the SlicerDMRI Extension (Use of Tractography Display)
### Notes
* Have +4GiB free of ram to run the program
* Have an algorithm to compute atlas-registration (e.g: DTI-Reg) to obtain the displacement field
* Program is running in background and write every outputs in the corresponding log file

## How does it work ?
Trafic is an extension made by two modules:
* TraficBi for the Biclassification
* TrafficMulti for the Multiclassification

Each Module has three tabs:
* The Edition Tab
* THe Training Tab
* The Classification Tab

### The Edition Tab
This tab permits to create a training data set or add some data to an existent one.
### The training Tab
The training tab permits to train our algorithm on a valid training data set. It is recommended to use the edition tab to create the dataset.
### The classification Tab
The classification tab, performs the actual classification using the model trained previously.

### TO DO
* Test the extension on Linux and on Mac
* Upgrade Polydata (new ITK and VTK version)
* Test CLI paths
* Add a verification for the training data set (must be valid i.e 2 folders for bi and 54 for multi)
* Use slicer.run to run CLI, instead of subprocess
## LICENSE
see LICENSE