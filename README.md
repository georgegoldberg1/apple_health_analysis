# README for apple_health_analysis

to explore zip file apple health data export

# Update Nov 2023: Added HRV Sleep Analysis

Heart Rate Variability Measurements are supposedly more accurate during Sleep.

The new notebook filters for HRV during sleep and plots the data.

# README for Base Python Docker

Builds ubuntu docker container, installing pip requirements for python and running jupyter notebook in your local browser.

Maps this repo folder into Docker so you can create and save notebooks and then git push outside of docker afterwards.

# Setup:

### Build and start container

`bash go.sh`

### Stop container

`bash stop.sh`  
(OR: `docker stop base_python`)
note: each time you run `bash go.sh`, it will stop the container that is currently running, so be careful if you havent saved changes in notebooks.

### Remove all stopped containers

`docker container rm $(docker ps -aq)`

## Optional:requirements.txt

You can change the packages in requirements.txt
After you run the container, it's recommended to do a pip freeze on the package versions, so this build will hold for future. Python version should be included too ideally.

## Version details

- python3.11 currently in ubuntu 22.04)
- Works on Apple Silicon.
- Updated Nov2023

## Author

George Goldberg
