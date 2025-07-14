# ESGF Compute Working Team Meeting - 2025-07-14


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  14/07/2025

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)
- David Huard (Ouranos)
- Maxwell Grover (ANL)
- Zach Price (ORNL)
- Forrest Hoffman (ORNL)
- Nils Hempelmann (ECMWF)

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

Max:
* new plugin for xarray: indexes
* one can index an arbitrary dimension
* https://xarray-indexes.readthedocs.io/index.html
* https://xarray-indexes.readthedocs.io/blocks/ndpoint.html
* could help clisops for geo/bbox subsetting

Zach:
* re-build roocs/wps version running in the ranger container environment
* now want to run this in OpenShift: kubernetes by RedHat

Nils:
* Florian Papenberger new director at ECMWF
* services at ECMWF will be closer in the future
* want to run the CLINT AI cycling tracking bird in production
* new project at ECMWF for climate indices
* going to FOSS4G tomorrow ... meet Tom Kralidis at pygeoapi workshop

Forrest:
* switch to ESGF2 shifted to end of August

David:
* want to use wearver + pywps for climate-indicies ... as production service
* pygeoapi still not ready for prdocution ... needs a better queueing system. 
* ... maybe use dask for queueing?

Carsten:
* updated clisops for S3 support
* working on PID system for ESGF2 ... consumes data publication requests from ESGF2 apache kafka queue


### 5. Next steps:

* Work on pygeopi and STAC. 
* Need a new cookiecutter and birdy. 
* Work on docker deployment. 
* Integrate with S3 storage. 
* Need a production ready (better queue) pygeoapi.

### 6. AOB:

Next meeting: 11th August 2025

