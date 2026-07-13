# ESGF Compute Working Team Meeting - 2026-07-13


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  13/07/2026

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)
- (all on vacation)

not attending:
- David Huard (Ouranos)
- Nils (ECMWF)
- Alessandro (KNMI)
- Sasha (LLNL)
- Zach Price (ORNL)
- Forrest Hoffman (ORNL)


## Agenda

### 1. Welcome and introductions

### 2. Actions and minutes from last meeting

- [ ] Carsten + David: work on pygeoapi + STAC
- [ ] Carsten: work on docker deployment
- [ ] Carsten etc: Write JOSS paper about Rook+clisops
- [ ] Carsten etc: WPS integration into STAC
- [ ] Carsten + David: add something for the compute service ... as PR (Sasha). Add David as reviewer.
    - https://github.com/WCRP-CMIP/cmip7-guidance/blob/docs/docs/CMIP7/Guidance_for_ESGF.md

### 3. Presentation (optional)

See list of presentations in issue https://github.com/ESGF/esgf-cwt/issues/35.

### 4. Discussion

#### Round Table

Nils:
* feedback from GA
* the different copernicus service need to work on common interfaces and usage patterns.

Here at 3:09 Chis talks about Enhanced C3S climate prediction and projection datasets and tools 
https://www.youtube.com/watch?v=1TgmCTyLPVM&t=11388s

David:
* ro-crate ... yaml with infos about where data is comming from


Carsten:
* woodpecker moved to roocs:
    * https://github.com/roocs/woodpecker
    * CDS people want to use it for new cmip6 decadal data
    * Integrated into Rook: 
    https://github.com/roocs/rook/blob/main/src/rook/fixes/providers/woodpecker.py
* started new test data repo:
    * https://github.com/cehbrecht/mini-climate-data
    * using recipes to build reduced test data from original data

### 5. Next steps:

* Work on pygeopi and STAC. 
* Need a new cookiecutter and birdy. 
* Work on docker deployment. 
* Integrate with S3 storage!!!
* Need a production ready (better queue) pygeoapi.
* Work on prov db for Rook WPS
* Write JOSS paper about Rook+clisops. See xclim example: https://joss.theoj.org/papers/10.21105/joss.05415
* WPS integration into STAC: https://github.com/ESGF/esgf-roadmap/issues/134

### 6. AOB:

Next meeting: 10th August 2026

