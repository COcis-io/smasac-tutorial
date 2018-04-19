# Social Media Analysis for Situation Awareness during Crises (SMASAC) Tutorial
![SMASAC](header.png "SMASAC")


Recent disasters and crises (such as Hurricanes Irma, Harvey and Maria) have affected many regions of the globe, causing damage in the billions of dollars and hundreds of lives. Communication technologies, such as social media, can play an important role in preventing some of this damage by helping first responders and humanitarian organizations mobilize resources effectively. Social media has emerged as a powerful tool for the crisis informatics community because it serves as a field-level, rich source of real-time information that would otherwise not be available.

Unfortunately, gaining situation awareness from social media content using semi-automatic methods is a difficult task due to the velocity, volume and noise associated with such data. In this tutorial, we will cover the primary steps that can be used for analysing crisis-related social media content in real-world crisis situations.

We will present a situation-awareness data analysis pipeline that focuses on some of the challenges that occur when dealing with social media, including steps ranging from data collection and filtering to event extraction and visualization. The methods, tools and lessons covered will draw on our real-world experience in crisis informatics research, and will include interactions and code demonstrations.


## Agenda and Slides
* Slides Part 1: Introduction: [pptx](slides/pptx/1-introduction.pptx)
* Slides Part 2: Crisis Data Collection and Filtering: [pptx](slides/pptx/2-data-collection.pptx)
* Slides Part 3: Concepts and Entities Extraction: [pptx](slides/pptx/3-entity-extraction.pptx)
* Slides Part 4: Classification and Categorisation: [pptx](slides/pptx/4-classification.pptx)
* Slides Part 5: Event Extraction: [pptx](slides/pptx/5-event-extraction.pptx)
* Slides Part 6: Visualisation: [pptx](slides/pptx/6-visualisation.pptx)


## Source Code and Notebooks
The tutorial hands-on sessions are mostly coded in Python and provided as Jupyter notebooks. The notebooks can be locally installed or visualsised online.

There is four different methods for runing and studying the notebooks:
1. Interactive notebook environment on mybinder
2. Rendered HTML notebooks on nbviewer (non-interactive)
3. Interactive local notebook environment:
    * Docker build or DockerHub (see below)
    * Native installation

## Notebooks
* Notebooks Part 1: Data Collection: [ipynb](notebooks/1-data-collection.ipynb) / [jupyter](http://127.0.0.1:8888/notebooks/1-data-collection.ipynb)

## Running and Installing the Notebooks
You can either run the tutorial using docker or installing all the required software manually. It is recommanded to use docker.



### Docker Installation
The [docker](https://docker.com/) installation is the recommended approach as it is more likely to work without any configuration issues.

#### Pull or Build Image
You can either pull the image directly from [Docker Hub](https://hub.docker.com) or build it from the source.

For installing the image from Docker Hub, you need to execute the following command:
```sh
docker pull evhart/smasac-tutorial
```

If you prefer you can clone this git repository and then build the image from the source using the following command:
```sh
docker build -t evhart/smasac-tutorial:latest .
```

#### Run Docker Image and Start Jupyter 
The Jupyter server can be started by starting the container using the following command:
```sh
docker run -it -p 8888:8888 --name smasac-tutorial evhart/smasac-tutorial:latest
```

Then, the Jupyter server should start and output the URI that needs to be used for connecting to the server. For example:
```
Copy/paste this URL into your browser when you connect for the first time,
    to login with a token:
        http://localhost:8888/?token=<SOME_TOKEN>
```

Simply copy the URI from your terminal into your web browser for accessing the Jupyter server.