# Project Description

The Windows on Earth program receives astronaut photos from the International Space Station (ISS). We know the location of the ISS when the photo was taken, but not what the photo is of. The subject is generally in a 300 mile radius of ISS location. 

This project seeks to use image recognition/machine learning combined with a virtual world simulator (we use Cesium) to attempt to geolocate the images automatically. We have a website at [Windows on Earth](https://www.windowsonearth.org/). 

Our goal is to accurately "predict" the location of the image. Specifically, we need the ability to recognize what the image is of, based on a simulated view of the world using things such as coastal or lake outlines, rivers, and other features. The system would need to "look around" in the simulation trying to match the photo to likely subjects (again, usually within 300 miles radius).

# Instructions to run the Final Pipelines

## How to build and run a docker container
- use the following command to build `docker build -t windows-on-earth .` the docker container
- run the docker container using the following command `docker run -p 8080:8080 windows-on-earth`
- open the link to the browser once the container is running or paste `http://localhost:8080/tree` in the browser
- if you had previously created the container do `docker start <replace by container id>` and open `http://localhost:8080/tree`

## How to run Pipeline-1-(NN)
- upload you query image in the [query_images](./query_images/) folder
- run the notebook [Poc_pipeline_NN.ipynb](./pipeline-1-(NN)/Poc_pipeline_NN.ipynb)
- enter the query image file name when prompted
- enter the mapbox access token when prompted

## How to run Pipeline-2-(SIFT)
- upload you query image in the [query_images](./query_images/) folder
- add the name of the query image in `Image` column of [results_SIFT_v2_csv.csv](./pipeline-2-(SIFT)/results_SIFT_v2_csv.csv)
- run the notebook [sliding_window_matcher_final_v3.ipynb](./pipeline-2-(SIFT)/sliding_window_matcher_final_v3.ipynb)
- enter the Google Maps API token when prompted
- view the identified location in [results_SIFT_v2_csv.csv](./pipeline-2-(SIFT)/results_SIFT_v2_csv.csv)

# Other Work
Find a detailed account of the other experimentation and research at [dev/README.md](./dev/README.md)

# Evaluations on the Pipelines

# Future Work and Suggestions:

# [Project Members](./COLLABORATORS)

- Hemant Kumar Singh
- Jaisal Singh
- Vedika Srivastava