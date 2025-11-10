# ESGF Compute Working Team Meeting - 2025-11-10


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  10/11/2025

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)
- David (Ouranos)
- Zach (LLNL)
- Forrest




- Nils Hempelmann (ECMWF)
- Alessandro (KNMI)


## Agenda

### 1. Welcome and introductions

### 2. Actions and minutes from last meeting

- [ ] Carsten + David: work on pygeoapi + STAC
- [ ] Carsten: work on docker deployment
- [ ] Carsten: add wiki page for presenters

### 3. Presentation (optional)

See list of presentations in issue https://github.com/ESGF/esgf-cwt/issues/35.

### 4. Discussion

#### Round Table

Carsten:
* Copernicus CDS wants to use regrid operator. Need to make a patch release in the next days of clisops.
* David: how is caching of grids done? 
    * predefined grids: https://github.com/roocs/roocs-grids/tree/main
    * caching grids in clisops: https://github.com/roocs/clisops/blob/2689a0b21a40859f81706503920cf956d77cd234/clisops/core/regrid.py#L1569

Forrest:
* showing the future architecture of ESGF at AGU (monday 15th of december): metagrid, esgf-search, ...

Zach:
* nothing new to report

David:
* some experimental work with weaver (has ogcapi interface): deploy cli tools as docker container, use cwl workflow, run everything in memory (no output written/read from disk)
* using pygeoapi in another project ... but pygeoapi queue is not ready for production ...

### 5. Next steps:

* Work on pygeopi and STAC. 
* Need a new cookiecutter and birdy. 
* Work on docker deployment. 
* Integrate with S3 storage. 
* Need a production ready (better queue) pygeoapi.
* Work on prov db for Rook WPS

### 6. AOB:

Next meeting: 8th December 2025

