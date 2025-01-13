# ESGF Compute Working Team Meeting - 2025-01-13


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  13/01/2025

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)
- David Huard (Ouranos)
- Nils Hempelmann (OGC)
- Zach Price (ORNL)
- Ben Coalson (ORNL)

## Agenda

### 1. Welcome and introductions

### 2. Actions and minutes from last meeting

- [x] Update calendar entry
- [x] Carsten: prepare new bird "Nandu" with pygeoapi on bird-house
- [ ] Max + Carsten: work on docker deployment
- [ ] Carsten: add wiki page for presenters
- [ ] Neil follow up with CEDA group about STAC + elasticsearch process

### 3. Presentation (optional)

See list of presentations in issue https://github.com/ESGF/esgf-cwt/issues/35.

### 4. Discussion

#### Round Table

Carsten:
* First bird Nandu with pygeoapi: https://github.com/bird-house/nandu
* need to finalize Nandu and then make a new cookiecutter and birdy for pygeoapi.
* later we also might need a slurm integration and replicacement for metalink (maybe STAC?).

David:
* plan to move to pygeoapi. need to find resources for it.
* PyWPS is still the stable version for production. pygeoapi is developed for the future in parallel.

Nils:
* updated the docs to use mkdocs/markdown.

Zach/Ben:
* we have issues with the regridding operator ... esmpy is not installed
* David: did you pip install esmpy? This might not work
* No further work done on Slurm installation


### 5. Next steps:

William likes to test the current docker deployment.

Work on pygeopi and STAC.

### 6. AOB:

Next meeting: 10th Feburary 2025

