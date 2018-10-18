# Flask2Docker - Simple counter site buildt on docker

## Components
  - Jenkins run on GCE as Container - available on http://35.242.226.117:8080
  - Docker slave runs on another GCE and published the flask on http://35.242.220.128:8000

## Flow
  1. The job is configured to receive a webhook from Github on push request
  2. Jenkins will pull the repository
  3. New docker image will be build and pushed to docker-hub
  4. The new image will be pulled and run on the docker host
