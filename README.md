# Brain Tumour Image Segmentation

A convolutional neural network for brain tumour image segmentation using the [U-Net architecture](https://link.springer.com/chapter/10.1007/978-3-319-24574-4_28).

## Segmentation Examples:
![](/screenshots/image1.png?raw=true)
![](/screenshots/image2.png?raw=true)
![](/screenshots/image3.png?raw=true)
![](/screenshots/image4.png?raw=true)

## Description
This is a convolutional neural network that performs brain tumour image segmentation by training the network using images of brain MRI scans from the [Medical Decathlon Challenge](http://medicaldecathlon.com/) dataset. The network is able to segment the images into either the background, an edema, a non-enhancing tumour or an enhancing tumour, and I used the U-Net architecture when making the segmentation class applied by the model during training. This project was very useful in learning how to apply computer vision techniques such as image segmentation as well as learning how to develop models using popular architectures such as U-Net for a real world application of computer vision.

## Model Evaluation:

The model works fairly well with a final training loss of ~0.0788 and a final test loss of ~0.1236 after 10000 iterations.

The model upon general inspection appears to do pretty well overall in detecting conditions. It is fairly good in determining if an edema is present in the scan, however the model at times may confuse the identification of enhancing tumours with non-enhancing tumours.

## Usage
The `segment.ipynb` notebook can be run locally or on [Google Colab](https://colab.research.google.com)
### Running on Colab:
Download the notebook and the tar file, upload the notebook to Colab, connect to a runtime, upload the tar file and then run all cells.
### Running locally:
Clone the repository, and run the notebook, ensuring you have numpy, matplotlib and pytorch installed. (Note: It will take longer to train the model locally as opposed to training on Google's GPU clusters on Colab).
