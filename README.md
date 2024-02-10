# Instagram Tech Stack

## Overview

This is a web app that built with Flask paired with Docker. Additonally, it uses Postgres for databases, and Gunicorn and Nginx for the production server. It is based on [this tutorial from testdriven.io](https://testdriven.io/blog/dockerizing-flask-with-postgres-gunicorn-and-nginx/). It core functioanlity allows one to upload media at [http://localhost:{port}/upload](http://localhost:{port}/upload). Once uploaded, they can view the image at [http://localhost:{port}/{image\_file\_name}](http://localhost:{port}/media/{image_file_name}).

![Screenshot](output.gif)


## Build Instructions

```
$ docker-compose up -d --build
```

```
$ docker-compose -f docker-compose.prod.yml up -d --build
```


