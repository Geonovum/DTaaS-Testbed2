# docker file voor ogc wps (pygeopapi) plus opentelemetry
# 

FROM geopython/pygeoapi:0.20.0

WORKDIR /pygeoapi

LABEL author='Niels Hoffmann'
LABEL name='ogc api and dcat'

ADD requirements.txt /pygeoapi/
RUN python3 -m pip install --no-cache-dir -r requirements.txt
