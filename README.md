# Self-Driving-Car
This is the code for Simulating a self driving car inspired by Siraj Raval's video on youtube.
See the ipython notebook provided for more details.

## Overview

I will be using Udacity's [Self driving car sim](https://github.com/udacity/self-driving-car-sim) for generating data for training and using as a car simulator while running the script. <br/>
Yu can download the pre-built simulator or download the Unity project from the repository provided above.

## Installtion

Install the dependencies using the configuration file given as :

```python
# Use TensorFlow without GPU
conda env create -f environments.yml 

# Use TensorFlow with GPU
conda env create -f environment-gpu.yml
```
Then activate the environment as 

```
source activate car-behavioral-cloning
```

Or install the dependencies using pip.

## Usage and running

I have provided a pretrained model which you can use. <br/>
Run the script as 

```python
python drive.py pretrained_model.h5
```
Then run the simulator in autonomous mode and see the script drive the car, you can see the calculated steering angles speed and other data displayed on the console.



## Training

For training on your own model you will need the data folder with images. This might take a while, for training on my GPU it took 7 CONTINUOUS HOURS!!!

```
python model.py
```
will generate models at every epoch, each better than the previous. <br/>
run the model as 

```python
python drive.py model-xxx.h5
```

