[![CircleCI](https://circleci.com/gh/agostonp/udproj-kubernetes.svg?style=svg)](https://circleci.com/gh/agostonp/udproj-kubernetes)

## Project Overview

In this project, I demonstrate the skills I have acquired to operationalize a Machine Learning Microservice API. 

I was given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project operationalizes a Python flask app that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

The project goal was to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications.
The following tasks were performed:
* Test project code using linting
* Complete a Dockerfile to containerize this application
* Deploy containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that the code has been tested


---

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Upload to Docker Hub: `./upload_docker.sh`
4. Run in Kubernetes:  `./run_kubernetes.sh`
5. Simple client to test the perdiction service: `./make_prediction.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl

### Other files in the repository

* .circleci/config.yml: build configuration for the cloud native continuous integration tool that is used for the validation of the project code
* model_data directory: `sklearn` model that has been trained to predict housing prices in Boston
* output_txt_files directory: sample out logs from a docker and a kubernetes run
* app.py: the main script containing the boilerplate code to execute the predictions in the model