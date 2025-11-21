# Topics

## Foundation

### Catalogues with Interoperable API's (5.1)

To achieve the goals of “no wrong door” when performing a federated search for data (aka resources), meaning: it does not matter in what catalogue you start your search for your data, you should always be able to find your data – when the catalogues are ‘connected’.

Catalogues come in various tastes and colours, and that is fine – however it is important that they can participate in a federation and find each other’s resources.

This topic also continues the development of the application store (aka the app store): making calculation modules (processes) usable as seamless and easy to use as possible. 

- __Task__
Add a software component to existing catalogues that expose an OGC API Records interface (this could be alongside other interfaces exposed by the service).

- __Deliverable__
A demo of a query to the catalogue, using OGC API Records, with a DCAT response, conforming to DCAT-AP-NL 3.0. 


### Sharing Data under Conditions, from a data consumer perspective (5.2)

Sharing data over secure webservices is a well understood pattern. Recently the EU introduced the concept of DataSpaces, protocols that allow data to be shared under conditions, conditions set forward by the data provider. Data users must agree with the conditions before they are granted access to the data. This contract negotiation is done on the so-called Control Plane of the DataSpace (The Data Plane in the DataSpace is the well know mechanism of webservices giving access to data).

In this research topic we would like to see a data consumer search, find, negotiate and bind to a dataset in a Dataspace, using Dataspace protocols (or similar, e.g. iShare and or FSC).


## Visualization

### Find and Bind (6.1)

Visualisation is an important aspect of a Digital Twin and is part of the basic expectation and user-experience with manipulating the Digital Twin to do policy making.

Many visualisation clients exist in the market, but each are made with a specific use-case or capability in mind. They all provide data (and results of calculation modules) and combine that data for insight and decision making. Importing the data is in some cases non-trivial, having to remember URLs, paths and queries. 

The goal is to make the data better findable in the visualization client, but also bindable: the ability to bring in the found data and bring it in as a “layer” with the least clicks as possible.

- __Tasks__
1.	Add a visualisation pane in the client, that displays the metadata of the relevant data, calculation modules (processes) and other resources that can be bound to from a (federated) catalogue. The pane has a search part to specify a query.
2.	The data (or processes, or resources) can be bound using the information in the metadata and shown in the client
3.	In case of processes, the ability to listen to callbacks and act accordingly (e.g. refresh events, request for new parameters, …)

- __Deliverables__
A demo of the visualisation client demonstrating the above.


### Export & import scenes (6.2)

Visualisation is an important aspect of Digital Twinning and is part of the basic expectation and user-experience interacting with the Digital Twin to do policy making.

Many visualisation clients exist in the market, but each is made with a specific use-case or capability in mind – and each one is very good at something, but not everything. Sometimes you start a scene in client A, because it is good in putting together the scene, then move on to client B to manipulate and do calculations in that client. 

Many clients lack the ability to export scenes and import them in another client. (clarification: this does not mean exporting data/vertices from the client, but the reference to the service that brought in the data, including the query)

The idea here is inspired by the (old) OGC WMS Context document (describing the state, or “Context,” of a WMS Client application in a manner that is independent of a particular client and that might be utilized by different clients to recreate the application state.), now extended to be used in 3D environments. 

- __Tasks__
1.	Define a prototype description of the elements that need to be exported from the scene to build up the scene in client B
a.	E.g.: reference to the web services that build the original scene, camera parameters, datetime, …
2.	Prototype the scene export in client A and optionally import the scene in client B
3.	Bring the proposal to the OGC for consideration

- __Deliverables__
1.	A (draft) schema of the scene
2.	A crude demo of the export/import


## Data

### BIM (Design information) for Digital Twins (7.1)

BIM models and design information (models) are an integral part of our depiction of the physical living environment, like Geo information.

Data sources include IFC models, GLTF/GLB, TIN, CityJSON (as a format in 3D Tiles). These encodings should be made available using web-services.

- __Task__
•	Describe how to make native IFC models available in Digital Twins using web services
•	Describe how to make transformed IFC models available in Digital Twins using web services

- __Deliverables__
•	Create a web service that serves IFC information to a 3D viewer in conjunction with non-BIM sources.
•	Call and show the BIM information in a 3D viewer in conjunction with non-BIM sources.


### Data downloads (7.2)

Albeit against the general idea of “data at the source”, data downloads (for local processing) remain a very popular usage pattern.  The OGC API’s do not offer a full dataset download, prevented by the client and server restrictions (e.g. pagination).

What is a good and efficient way to provide a full dataset download? Through (a modified) OGC API (Features) or through alternative, parallel alternatives (e.g. Atom feeds, direct downloads, ...)?

This is also in support of the INSPIRE download service.

> This topic is not addressed during the testbed.

## Calculation models

###  Making calculation modules interoperable using OGC API Processes (8.1)

Calculation modules make up an important part of a Digital Twin, allow for simulation, time-travels etc. Having these functions available as an online interoperable service is a critical success factor for the ease of use of a Digital Twin – and – to allow for machine-machine (via API’s) communication.

- __Tasks__
1.	Add a software component to an existing calculation model that exposes a full implementation of the OGC API Processes (Part 1: Core).
a.	Compliant with the OGC specification 
i.	Async process execution
ii.	Including fully working callbacks

- __Deliverables__
A working implementation of a calculation model using OGC API Processes.


### Model orchestration, status quo

Calculation models serve an important role in Digital Twins: they allow for simulation, time travel etc. A single model is powerful, but chaining models is where the true added value lies. E.g. a weather model that feeds into a traffic model that feeds into e.g. a traffic rerouting plan.

What is possible today (the status quo) to achieve model orchestration (chaining), using what techniques or what standards really work?

- __Task__
Describe today’s status quo on model orchestration.

As this topic is possibly very large and deep, restrict the research to coupling 2 models: E.g. a meteorological model predicts excessive rain in a certain area – and to avoid traffic chaos in that area, takes the outcomes from the meteorological model and feed it as input into a traffic model. The outcomes of the traffic model will allow policy makers to shutdown roads and reroute traffic.

- __Deliverables__
A report describing the various standards and techniques, including a maturity model.
