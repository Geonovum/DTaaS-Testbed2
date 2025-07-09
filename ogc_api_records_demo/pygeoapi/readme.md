# OGC API Records demo

This folder contains a pygeoapi server configured with an OGC API Process, OGC API Features and OGC API Records offering.

The OGC API Records shows a possible implementation for DCAT-AP-NL 3.0

The OGC API Process and Features are implemented to demonstrate the interdependencies between the services.

--

requirements: Docker and Docker compose

run: ```docker compose up```

This will build a pygeoapi docker image (based on version 0.20.0) with additional python libraries for the OGC API Process.

Once the docker container is running the site can be visited at http://localhost:5000/

--

the client.ipynb jupyter notebook demonstrates how to use the OGC API's

In the dcat folder samples and code is available to load the tinyDB catalogue that is used with OGC API Records