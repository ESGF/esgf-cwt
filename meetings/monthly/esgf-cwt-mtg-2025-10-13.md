# ESGF Compute Working Team Meeting - 2025-10-13


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  13/10/2025

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)
- Nils Hempelmann (ECMWF)
- Alessandro (KNMI)


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

Alessandro:
* was very busy with general assemblies and reporting
* involved in new projects concerning provenance

Nils:
* fair tool: https://www.f-uji.net/
* ecmwf tries to get 100% fair coverage: https://www.ecmwf.int/en/newsletter/183/news/towards-fairer-data-stores-service
* involved in climate europe 2

Carsten:
* still working on the PID service (piddiplatsch) to make it ready for CMIP7
* interested in setting up a provenance database for the WPS rook:
* Alessandro: 
    * we are using neo4j, triple import of prov docs, using cipher for queries
    * you need to define templates (with knowledge of the prov model) to run queries


### 5. Next steps:

* Work on pygeopi and STAC. 
* Need a new cookiecutter and birdy. 
* Work on docker deployment. 
* Integrate with S3 storage. 
* Need a production ready (better queue) pygeoapi.
* Work on prov db for Rook WPS

### 6. AOB:

Next meeting: 10th November 2025

