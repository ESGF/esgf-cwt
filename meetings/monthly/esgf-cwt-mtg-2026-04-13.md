# ESGF Compute Working Team Meeting - 2026-04-13


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  13/04/2026

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)
- Nils (ECMWF)
- Sasha (LLNL)
- David (Ouranos)

- Zach Price (ORNL)
- Forrest Hoffman (ORNL)
- not available: David Huard (Ouranos)
- not available: Alessandro (KNMI)

## Agenda

### 1. Welcome and introductions

### 2. Actions and minutes from last meeting

- [ ] Carsten + David: work on pygeoapi + STAC
- [ ] Carsten: work on docker deployment
- [ ] Carsten etc: Write JOSS paper about Rook+clisops
- [ ] Carsten etc: WPS integration into STAC

### 3. Presentation (optional)

See list of presentations in issue https://github.com/ESGF/esgf-cwt/issues/35.

### 4. Discussion

#### Round Table

Sasha:
* https://github.com/WCRP-CMIP/cmip7-guidance
* https://github.com/WCRP-CMIP/cmip7-guidance/blob/docs/docs/CMIP7/Guidance_for_ESGF.md
* TODO: please add something for the compute service ... as PR. Add David as reviewer.

Alessandro:
* status of WPS in ESGF-NG?
* Carsten: need to query the new STAC catalog to get the dataset ID (instead of the ESGF index)

Nils:

* prep Copernicus/ECMWF GA in Budapest in June
* ECMWF will open a ticket system for users soon

Carsten:
* woodpecker demo continued:
    * https://github.com/cehbrecht/woodpecker
    * Demo for fixing library ... inspired by Ruff Python linter
    * bi-weekly meeting with Ag (CEDA) and Bouwe (ESMValTool) for further development
    * Simple API, supports workflows
    * next: 
        * add database support? use DuckDB ???
        * support plugins: pluggy, entrypoint (part of python library)
* David: 
    * Users should be able to open a ticket on github and a fix can be provided via PR
    * keep in mind that the xarray lib is "unstable" ... api can change with new versions


### 5. Next steps:

* Work on pygeopi and STAC. 
* Need a new cookiecutter and birdy. 
* Work on docker deployment. 
* Integrate with S3 storage. 
* Need a production ready (better queue) pygeoapi.
* Work on prov db for Rook WPS
* Write JOSS paper about Rook+clisops. See xclim example: https://joss.theoj.org/papers/10.21105/joss.05415
* WPS integration into STAC: https://github.com/ESGF/esgf-roadmap/issues/134

### 6. AOB:

Next meeting: 11th May 2026

