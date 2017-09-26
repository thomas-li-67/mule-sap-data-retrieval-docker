App specific Mule ESB Enterprise Docker Image
===============

This project contains a Dockerfile for the deployment and packaging of a standalone Mule ESB Enterprise with Docker.

Preparing the Docker base image
---------------


Hence the directory should look like this:
* mule-sap-data-retrieval/
* mule-sap-data-retrieval/Dockerfile
* mule-sap-data-retrieval/sap-fi-data-retrieval-v1.0-with-internet.zip


Building and tagging the Docker base image
---------------

```bash
docker build --tag="thomas67/mule-sap-data-retrieval" .
```


App specific Mule ESB Enterprise Container
---------------

Start app specific image:

```bash
docker run -t -i -p 8081:8081 --name='mule-app-node' thomas67/mule-sap-data-retrieval
or
docker run -d -p 8081:8081 --name='mule-app-node' thomas67/mule-sap-data-retrieval
```