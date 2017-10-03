# rt106-rad-seed
Seed application for radiology.

### To build the Docker image

To build the docker container for the rad seed:

    $ docker build -t rt106/rt106-rad-seed:latest .

If you use HTTP proxies in your environment, you may need to build using

    $ docker build -t rt106/rt106-rad-seed:latest  --build-arg http_proxy=$http_proxy --build-arg https_proxy=$https_proxy  --build-arg no_proxy=$no_proxy .

### Configuring a database

### Downloading demo data (optional)
The datastore service (rt106-datastore-local) is configured to download and serve a portion of the Visible Human Dataset.

### Configuring local environment

Create a file called ```.env``` and set the path to your local datastore

```
LOCAL_DATA_DIR=/PathToLocalDatastore
```

### To run the rad seed application

To run the rad seed application

```
$ docker-compose up
```

Web pages for the application are served on port 81
