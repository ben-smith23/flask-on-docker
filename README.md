# Instagram Tech Stack

## Overview

This is a web app that built with Flask paired with Docker. It uses Postgres for databases, and Gunicorn and Nginx for the production server. It is based on [this tutorial from testdriven.io](https://testdriven.io/blog/dockerizing-flask-with-postgres-gunicorn-and-nginx/). It core functionality allows one to upload media at [http://localhost:{port}/upload](http://localhost:{port}/upload). Once uploaded, they can view the image at [http://localhost:{port}/media/{image\_file\_name}](http://localhost:{port}/media/{image_file_name}). The tech stack is intended to resemble Instagram's.

![Screenshot](output.gif)


## Build Instructions

To build the images and run the containers in the development server, run the following command:

```
$ docker-compose up -d --build
```

The development build mounts the web folder in the container, allowing for automatic updates.


- docker-compose: Runs multi-container Docker apps.
- up: Runs containers.
- -d: Runs containers in the background.
- --build: Builds images.

To do the same for the production server, run the following command, which uses the docker-compose.prod.yml file:

```
$ docker-compose -f docker-compose.prod.yml up -d --build
```

The production build uses Gunicorn and Nginx. Unlike the development server, you must rebuild the image to apply changes.
