# External Software for DCAN Labs nhp-abcd-bids-pipeline-synth.
The repository contains the Dockerfile to create a Docker image of external
software packages used by the DCAN nhp-abcd-bids-pipeline-synth pipeline.
Notice that there is no entry point for this container.

## Installation
In order to run this software via a container, you will need to acquire a copy
of the FreeSurfer License for yourself from:

[Follow this link for a FreeSurfer
License](https://surfer.nmr.mgh.harvard.edu/fswiki/License)


## Using Docker
Before running, you will need to load the image onto your Docker service by
running the following command:
```
docker pull dcanumn/external-software-nhp-synth
```
If you receive a "no space left on device" error during this pull process, you
may need to clean up any old/dangling images and containers from the docker
registry, and possibly increase the amount of space allocated to Docker.

## Using Singularity
You can either pull the image from the Docker repository or build it from the
repository for the image to be saved in the working directory:
```
singularity pull docker://dcanumn/external-software-nhp-synth

singularity build external-software.img docker://dcanumn/external-software-nhp-synth
```
These are essentially the same, but in the latter case you have control over the
name of the file.


