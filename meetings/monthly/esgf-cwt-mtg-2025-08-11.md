# ESGF Compute Working Team Meeting - 2025-07-14


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  11/08/2025

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)
- David Huard (Ouranos)
- Nils Hempelmann (ECMWF)
- Zach Price (ORNL)
- Maxwell Grover (ANL)

## Agenda

### 1. Welcome and introductions

### 2. Actions and minutes from last meeting

- [ ] Carsten + David: work on pygeoapi + STAC
- [ ] Max + Carsten: work on docker deployment
- [ ] Carsten: add wiki page for presenters

### 3. Presentation (optional)

See list of presentations in issue https://github.com/ESGF/esgf-cwt/issues/35.

### 4. Discussion

#### Round Table

Nils:
* visited European FOSSGIS, Bosnien, small one
* meet Tom Kralidis ... pygeoapi
* Tom ... thinks about building a formal european organisation ...
* the ESA might take over some of the community work done by OGC
* ESA is already funding/supporting FOSS4G software ... need a european slim organisation to make it easier.
* OGC has changed ... moving to industrial focused topics
* OSGeo might get a higher importance
* Nils in contact with WMO for climate services ... also with Tom Kralidis (pygeoapi) ... Barcelona Super Computer is running the project, ECMWF involved

Max:
* pywps service is up and running again
* I will leave the lab end of august ...

Zach:
* worked on the wps service

David:
* working with Francis on weaver (wrap wps to ogcapi). wrote CLI to build new services ... which could than be deployed as a docker ... using ogcapi ...

Carsten:
* working on the PID service for ESGF2
* Question to Zach: how to deal with the STAC patches comming from the Kafka queue? 

### 5. Next steps:

* Work on pygeopi and STAC. 
* Need a new cookiecutter and birdy. 
* Work on docker deployment. 
* Integrate with S3 storage. 
* Need a production ready (better queue) pygeoapi.

### 6. AOB:

Next meeting: 8th September 2025

