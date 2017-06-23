#Normally installed google cloud sdk with ability to install additional packages
Not based on official image

## Normal run

`docker run -it maxmtmn/installer-based-google-cloud-sdk:latest`

## Run with mount current directory

`docker run -it -v $PWD:$PWD -w $PWD maxmtmn/installer-based-google-cloud-sdk:latest`

## Install additional modules

`gcloud --quiet components install kubectl beta docker-credential-gcr`

## Update

`gcloud --quiet components update`

## Rebuild with custom version of google cloud sdk
Use --build-arg or environment variables kube_aws_version and kubectl_version. Example:
`docker build --build-arg CLOUDSDK_VERSION=158 -t maxmtmn/installer-based-google-cloud-sdk .`