# Visual Speech Recognition


***This repository contains code that facilitates research on the impact of the [Lombard effect](https://en.wikipedia.org/wiki/Lombard_effect) on Visual Speech Recognition models.***

## Introduction
Visual Speech Recognition (VSR) is a field of research that focuses on recognizing speech from visual cues, 
such as lip movements and facial expressions. 
The Lombard effect refers to the phenomenon where speakers involuntarily modify their speech production in noisy environments by increasing their vocal effort, 
amplitude, and articulatory movements. This effect can have implications for VSR models, as the visual cues may change due to the speaker's adaptation to the noisy conditions.


## Getting Started
##### **Prerequisites**
Before running the code, you need to install the necessary libraries and dependencies listed in the `requirements.txt` file.

**Note:** Make sure to change the CUDA version for [PyTorch](https://pytorch.org/) in `requirements.txt` file to 
match your specific requirements if you intend to use GPU acceleration.

To install the required dependencies, run the following command:

```
pip install -r requirements.txt
```

##### **Problems you may encounter and how to solve them**
One of the notebooks(`lip_and_mouth_extraction.ipynb`) uses [dlib](http://dlib.net/) library and 
the installation process for this one may differ from one device to another, 
so in case you need to run only that notebook we highly recommend using [Google colab](https://colab.research.google.com/)
as for the time of writing this `README` it is already installed there, and you will avoid possible struggles with the installation.

Another problem you may encounter is the file structure you have to follow to make the code work. 
We tried our best to make the structure as available as possible leaving the directories and subdirectories in the repository, 
so the only you should do is to follow the instructions in `main.ipynb` file.  

## Repository Structure
The repository is organized as follows:

#### Main directories:
`data/` - this directory contains raw data that need to be preprocessed and compressed data that needs to be unpacked.
`clean_data/` - this directory contains cleaned data that was preprocessed and may be used to train models or help in training models somehow.
`LIPNET_original_weights/` - this directory contains weights that were shamelessly taken from [GitHub repo](https://github.com/VIPL-Audio-Visual-Speech-Understanding/LipNet-PyTorch)
`logs/` - this directory contains log files used by tensorboard and is divided into sections for validation logs(all train logs are in `logs/` directory itself).
`weights/` - this directory contains files with weights for our models. To get better understanding of versions you should review `main.ipynb` file.

#### Main notebooks:
`main.ipynb` - notebook that has data preprocessing, model definition and training.
`lip_and_mouth_extraction.ipynb` - notebook that has lip and mouth extraction scripts. Read it to get more insights.

## DEMO
The demo of the best model trained here can be found in [GitHub repo](https://github.com/mfedkiv/nn-course-work)
