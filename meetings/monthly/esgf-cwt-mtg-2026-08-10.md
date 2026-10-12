# ESGF Compute Working Team Meeting - 2026-08-10


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  10/08/2026

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
- Ag (CEDA/STFC)


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


Carsten:
* rook/CDS:
    * cordex avail via rook with subsetting
    * heavy load like 10Ks requests per day
    * some jobs get stuck ... stalled. Add cronjobs to remove and report bag stalled jobs.
* woodpecker moved to roocs:
    * https://github.com/roocs/woodpecker
    * CDS people want to use it for new cmip6 decadal data
    * conda package now available
    * presentation at eRise/Futura meeting in Milan
    * running in production node now for CDS
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

Next meeting: 12th October 2026

