## Introduction
This repository contains various tutorials written for DataCamp. 

## How to run code?
I like to keep the Python setup in my OS very simple and create virtual environments with required custom libraries depending on the project I want to run. I would very much like to use Docker for this purpose, as that is the de-facto standard for process isolation. However since I am using Windows there is no way for me to expose my GPU to Docker. Thus, I opt to `conda` and Python virtual environment.

### Using conda environment
1. Download and install [Anaconda](https://www.anaconda.com/download/#windows)
2. Make sure conda is in the system PATH by trying `conda --version` on a terminal
3. Create a conda virtual environment using `conda create -n datacamp.tutorials python=3.5`
4. `cd` into the project directory
5. Install tensorflow as follows
	* If you **do not** have a GPU use: `conda install -n datacamp.tutorial --yes --file requirements.txt`
	* If you **do** have a GPU use: `conda install -n datacamp.tutorials --yes --file requirements_gpu.txt`
6. Activate the newly created environment with `activate datacamp.tutorials`
	
Further reading on how to setup conda environments: [Here](https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/20/conda/)

### Using Python virtualenv
