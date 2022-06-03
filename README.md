# Manessia Knowledge Base

## Overview
This repository contains all files used to create the [Manessia KB](https://kg.manessia.ch/) website. Automatic deployment happens with Netlify.

## Deployed Documentation
Check it out [here](https://kb.manessia.ch/)

## Local Development and Testing with Docker

1. Clone the repo locally and `cd` into it.
2. Download the docker image with `docker pull squidfunk/mkdocs-material`, then build the custom docker image with `docker build -t squidfunk/mkdocs-material .`
3. run `docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material` to start the dev server
4. run `docker run --rm -it -v ${PWD}:/docs squidfunk/mkdocs-material build` to build the site to /site
