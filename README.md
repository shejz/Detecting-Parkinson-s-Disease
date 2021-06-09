## Detecting Parkinsons Disease

Detect Parkinson’s disease in geometric drawings (specifically spirals and waves) using OpenCV and computer vision. We utilized the Histogram of Oriented Gradients image descriptor to quantify each of the input images.

After extracting features from the input images we trained a Random Forest classifier with 100 total decision trees in the forest, obtaining:

**83.33%** accuracy for spiral
**71.33%** accuracy for the wave

It’s also interesting to note that the Random Forest trained on the spiral dataset obtained 76.00% sensitivity, meaning that the model was capable of predicting a true positive (i.e., “Yes, the patient has Parkinson’s”) nearly 76% of the time.

### What is Parkinson’s disease?

![]()

Parkinson’s disease is a nervous system disorder that affects movement. The disease is progressive and is marked by five different stages:

- **Stage 1**: Mild symptoms that do not typically interfere with daily life, including tremors and movement issues on only one side of the body.
- **Stage 2**: Symptoms continue to become worse with both tremors and rigidity now affecting both sides of the body. Daily tasks become challenging.
- **Stage 3**: Loss of balance and movements with falls becoming frequent and common. The patient is still capable of (typically) living independently.
- **Stage 4**: Symptoms become severe and constraining. The patient is unable to live alone and requires help to perform daily activities.
- **Stage 5**: Likely impossible to walk or stand. The patient is most likely wheelchair bound and may even experience hallucinations.

We’ll be leveraging the fact that two of the most common Parkinson’s symptoms include tremors and muscle rigidity which directly impact the visual appearance of a hand drawn spiral and wave.

The variation in visual appearance will enable us to train a computer vision + machine learning algorithm to automatically detect Parkinson’s disease.

### The spiral and wave dataset

![]()

The dataset we’ll be using here today was curated by Adriano de Oliveira Andrade and Joao Paulo Folado from the [NIATS of Federal University of Uberlândia](http://www.niats.feelt.ufu.br/en/node/81).

The dataset itself consists of 204 images and is pre-split into a training set and a testing set, consisting of:

- **Spiral**: 102 images, 72 training, and 30 testing
- **Wave**: 102 images, 72 training, and 30 testing
