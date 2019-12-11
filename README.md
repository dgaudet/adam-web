# adam-web

## Publish your code to google app engine
* Spin up the latest alpine version of the google cloud sdk container
* Go to the root of the app in terminal
* docker run --mount type=bind,source="$(pwd)"/website,target=/app -it google/cloud-sdk:alpine /bin/ash
* Authenticate
* gcloud auth login
* Deploy the app
* cd /app
* Push code without directing traffic
* gcloud app deploy --project apbtoolsales-web --no-promote
* Push and direct traffic
* gcloud app deploy --project apbtoolsales-web