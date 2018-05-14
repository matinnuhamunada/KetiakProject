# Getting Started for the Lab Members
This folder contains the script to mine data from EBI-Metagenomics portal and gather the analysis result to do comparative analysis of human skin microbiome. We will use `Jupyter Lab` on `Python 3` with Windows 10 and Github to collaborate. Please contact me at matin_nuhamunada@gmail.com to be added to the repository.

## Install Anaconda
Install the latest `Anaconda` with `Python 3` from https://www.anaconda.com/download/

## Install Jupyter Lab
Open `Anaconda Navigator` and install `Jupyter Lab` or use `conda`
```bash
conda install -c conda-forge jupyterlab
```
You can also follow the instruction from http://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html

## Install Github Desktop
Create an account and install the latest Github Desktop from https://desktop.github.com/

## Setting Your Jupyter Lab directory
Findout where is your default working directory. You can check it using `python` with this command
```python
import os
os.getcwd()
```
You can change your `Jupyter Lab` directory by using Jupyter config. First create the directory you wanted to move in (we usually use `D:\Jupyter` as our working directory). Then, using `Anaconda Prompt` type
```bash
jupyter notebook --generate-config
```
Go to the default directory, and find the `.Jupyter directory`. Inside, you'll find the `jupyter_notebook_config.py` and using any text editor, uncomment the directory configuration line to this
```python
## The directory to use for notebooks and kernels.
c.NotebookApp.notebook_dir = 'D:\Jupyter'
```
## Clone the repository to your Jupyter Folder
After getting the invitation to collaborate, you can clone and contribute to our project. Open `Github Desktop` and create new repository by cloning this project to the `Jupyter` directory
