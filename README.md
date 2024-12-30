# adam-web

## Publish your code to google app engine
* Spin up the latest version of the Google CLI container - https://cloud.google.com/sdk/docs/downloads-docker
```shell
docker pull gcr.io/google.com/cloudsdktool/google-cloud-cli:496.0.0-stable
```
* Go to the root of the app in terminal
```shell
docker run --rm \
  --volume "$(pwd)"/website:/app \
  -it gcr.io/google.com/cloudsdktool/google-cloud-cli:496.0.0-stable /bin/sh
```
* Authenticate
```shell
gcloud auth login
```
* Deploy the app without directing traffic to test it out
```shell
cd /app
# Push code without directing traffic
gcloud app deploy --project apbtoolsales-web -v 1-0 --no-promote
```
* Deploy the app and direct traffic (from the app directory)
```shell
gcloud app deploy --project apbtoolsales-web
```˚