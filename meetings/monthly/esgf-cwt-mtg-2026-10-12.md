# ESGF Compute Working Team Meeting - 2026-10-12


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  12/10/2026

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)


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

Alessandro was at Milano for eRise and Futura (ESGF-NG) general assembly:

* Bryan working on active storage    
    * https://github.com/NCAS-CMS/PyActiveStorage
* using DASK for accessing S3 storage. Karsten did a demo about access mode ...  
* Milano linkedin:
    * https://www.linkedin.com/company/futura-horizon-europe/

Carsten:
* rook for ESGF-NG in Milano:
    * https://roocs.github.io/rook/talks/milano-2026
* woodpecker for ESGF-NG, ESMValTool and CDS in Milano:
    * https://roocs.github.io/woodpecker/talks/milano-2026
    
Nils:

* working on deliverable for climate-europe 2

### 5. Next steps:

* Work on pygeopi and STAC. 
* Need a new cookiecutter and birdy. 
* Work on docker deployment. 
* Integrate with S3 storage!!!
* Need a production ready (better queue) pygeoapi.
* Write JOSS paper about Rook+clisops. See xclim example: https://joss.theoj.org/papers/10.21105/joss.05415
* WPS integration into STAC: https://github.com/ESGF/esgf-roadmap/issues/134
* Use Rook for ESGF-NG
* Work on Woodpecker

### 6. AOB:

Next meeting: 9th November 2026

