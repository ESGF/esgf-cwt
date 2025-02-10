# ESGF Compute Working Team Meeting - 2025-02-10


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  10/02/2025

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)
- David Huard (Ouranos)
- Nils Hempelmann (OGC)
- Alessandro Spinuso (KNMI)
- Zach Price (ORNL)
- Jitu Kumar (ORNL)

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

Carsten:
* working with Trevor on strop/clisops/daops
    * strop: core functionality of clisops
    * clisops ... everything else that is needed by Rook/ECMWF
    * daops: updated to latest versions ... skip roocs_utils. Maybe skip daops in the future? Everything still used can be moved to either clisops or rook.

David:
* nothing to report

Nils:
* clean up docs for clint ... glossary, bibliography
    * https://birdhouse2-docs.readthedocs.io/en/latest/
* working on copernicus components ... land monitoring service
* code sprint (copernicus, esmwf, land monitoring) ... moving to pygeoapi or zoo, cwl workflow language

Alessandro:
* updating this doc: WMO-No. 1131 — Climate Data Management System Specifications (CDMS)
* meeting last week: auth users, ESGF, EGI checkin, for Europe to access ESGF services, to publish data and also to access notebook environments + computional services + etc ...

Jitu/Zach:
* working on deployment of Rook/WPS
* look into slurm for WPS to be able to handle the load
* had some issues with pip packages ... need to use conda
* pygeoapi might make it easier to provide status infos from slurm nodes

### 5. Next steps:

Work on pygeopi and STAC. Need a new cookiecutter and birdy.

### 6. AOB:

Next meeting: 10th March 2025

