# Setup Guide

## Installation
- Install Cuda Toolkit (tested with version 10.0)
- Install Anaconda
- Create Conda env (tested with version python 3.7.4)
- `activate <env_name>`
- run `conda install pytorch torchvision cuda100 -c pytorch`
- run `conda install numpy opencv`
- run `pip install imutils` 

## Run
- cd <repo_root>/fast_neural_style/
- activate <env_name>
- python neural_style/neural_style.py eval --cuda 1

## Controls
- <kbd>P</kbd> : Pause / Unpause
- <kbd>A</kbd> : Previous style
- <kbd>D</kbd> : Next style
- <kbd>Q</kbd> or <kbd>Esc</kbd>  : Quit

## Training
- download dataset (example: [coco](http://cocodataset.org/#download)) and extract it to <repo_root>/fast_neural_style/dataset
    - it das to be a folder containing a folder containing a lot of images
- choose a style image

- `cd <repo_root>/fast_neural_style/`
- `activate <env_name>`
- `python neural_style/neural_style.py train --dataset dataset --style-image <path/to/style/image> --save-model-dir <model/output/path> --epochs 2 --cuda 1
