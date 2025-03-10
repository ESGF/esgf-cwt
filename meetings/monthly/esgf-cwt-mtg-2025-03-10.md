# ESGF Compute Working Team Meeting - 2025-03-10


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  10/03/2025

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)
- Ben Coalsen (ORNL)
- David Huard (Ouranos)
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
* still working on cleanup of clisops
* moved to latest version of xarray ... but this breaks the regridding operator.
    * https://github.com/pydata/xarray/issues/7794
* atlas-v2 in the making for publishing into Copernicus CDS ... data gets synced at IPSL and DKRZ


Ben/Zach/Jitu:
* We had some issues with the pip installation ... no going back to conda.
* Conda "default" channel is restricted now. We can only use conda-forge.
* CE: latest version of Rook only uses conda-forge.

David:
* having a new processing service for climate indices with pygeoapi
* https://pavics.ouranos.ca/portail-ing-backend/
* github repo is still private: access can be given on request (GitHub ID)
* working on using S3 storage (minio) for outputs

### 5. Next steps:

Work on pygeopi and STAC. Need a new cookiecutter and birdy.

### 6. AOB:

Next meeting: 14th April 2025

