# jetson_asl

This is a PyTorch-based Jupyter Notebook designed to generate a classification model for the purpose of identifying ASL alphabet characters. The Notebook was tested on the Jetson Nano, fully utilizing its PyTorch CUDA acceleration capabilities.
Although the Notebook is currently configured and written for the generation of a classification model for classifying ASL alphabet characters, the Notebook is fairly flexible and may be easily modified to any image-based classification problem. 
Classes are determined by the dataset file structure, and any number of input images may be used for training. Additionally, simple visualization capabilities are included as well. 
This Notebook relies on the pre-trained ResNet-18 model as its basis, and modifies its fully connected layers to allow for transfer of the pre-trained model to the task of classifying ASL alphabet characters.

## File Structure
- `sign_language.ipynb`: The main Jupyter Notebook for the generation of the classification model
- `utils.py`: Dependency of the main Notebook, taken from NVIDIA DLI course materials.
- `mymodel.h5`: Example model output of the Notebook, included for reference.
- `README.md`: This file containing documentation of this project.
- `data/`: Skeleton directory to place the dataset (not included). Instructions for obtaining the dataset are included in the README within this directory.

## Hardware and Software Prequisites
1. NVIDIA Jetson Nano Developer Kit
2. NVIDIA DLI Nano Docker Container with matplotlib installed
3. Kaggle account to obtain ASL alphabet dataset

## Execution Instructions
First, prerequisites must be resolved. Once you have obtained an NVIDIA Jetson Nano Developer Kit, follow the instructions included in [this link](https://catalog.ngc.nvidia.com/orgs/nvidia/teams/dli/containers/dli-nano-ai) to setup and run the NVIDIA DLI Nano Docker container. 
When you first enter the Docker container's command line, there will be a printout referencing a local address where the Jupyter Notebook instance will be started. Keep note of this address for future use.
One prerequisite of this project is not included within the container by default. Once you enter the command line interface of the Docker container, enter `pip3 install matplotlib` to obtain this additional prerequisite. 

Once the Docker container is up and running, clone this repository to a location within the Docker container. Additionally, the dataset must be downloaded and placed within the `data/` directory of this repository on the Docker container.

Finally, the `sign_language.ipynb` file may be run. Access the Jupyter Notebook interface automatically started with the NVIDIA DLI Nano Docker container through the local address printed onto the terminal at Docker container startup.
Within the `sign_language.ipynb` file, click run all to generate a model. This process may take several hours.  
