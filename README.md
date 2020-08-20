[![mahdiuzzaman](https://circleci.com/gh/mahdiuzzaman/project-ml-microservice-kubernetes.svg?style=svg)](https://app.circleci.com/pipelines/github/mahdiuzzaman/project-ml-microservice-kubernetes?filter=mine)

# Summary
A pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). A Python flask app, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.


# How run the project
## Directly running in localhost/linux machine
* Install python 3.7 by running `sudo apt install python3.7` 
* Go to project directory
* Run `make setup`
* Run `source ~/venv/.devops/bin/activate`
* Run `make install`
* Run `python app.py`
* Run `./make_prediction.sh` to get pprediction result


## Inside a Docker COntainer
* Install docker
* Run `./run_docker.sh`
* Run `./make_prediction.sh` to get pprediction result


## Inside Kubernetes
* Install kubectl and minikube
* Run `./run_kubernetes.sh
* Run `./make_prediction.sh` to get pprediction result


# File Structure

├── app.py  ==> Flask app\
├── Dockerfile ==> Used for creating dockerimage\
├── Makefile ==> Used for Easy setup and testing\
├── make_prediction.sh ==> Contains JSON payload for get prediction form app.py\
├── output_txt_files\
│   ├── docker_out.txt ==> terminal output after running docker container and make_prediction.sh \
│   └── kubernetes_out.txt ==> terminal output after running dkubernetes cluster and make_prediction.sh \
├── README.md \
├── requirements.txt ==> Python dependency for Flask app\
├── run_docker.sh ==> set of shell command for creating docker image and container\
├── run_kubernetes.sh  ==> set of shell command for running kubernetes cluster \
└── upload_docker.sh  ==> set of shell command for uploading docker image to Dockerhub



