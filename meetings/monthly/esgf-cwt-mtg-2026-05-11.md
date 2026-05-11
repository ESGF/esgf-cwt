# ESGF Compute Working Team Meeting - 2026-05-11


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  11/05/2026

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)
- David Huard (Ouranos)
- Alessandro (KNMI)
- Nils (ECMWF)

not attending:
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
* prepareing CDS GA, 3-5 june, Budapest
* https://climate.copernicus.eu/9th-c3s-general-assembly
* open for online access
* involved with Alessandro on quality tool for CDS

David:
* involved in the atlas data group
* https://cds.climate.copernicus.eu/datasets/multi-origin-c3s-atlas?tab=overview
* atlas: they will use xclim and xarray for next version
* goldfinch: preparing ogcapi interface for it ... not sure if it will be pygeoapi or the ogcapi adapter by crim
* interested in joining the CDS GA online

Alessandro:
* is the new ESGF2 alive? ... nobody knows ... all silent
* interested in joining the CDS GA online

Carsten:
* woodpecker demo continued:
    * https://github.com/cehbrecht/woodpecker
    * Demo for fixing library ... inspired by Ruff Python linter
    * bi-weekly meeting with Ag (CEDA) and Bouwe (ESMValTool) for further development
    * Features: 
        * Fix (Python), 
        * FixPlan (json, fixes for a dataset), 
        * FixPlanStore (storing fix plans to querry them)
        * plugins with "entrypoint" to provide fixes packages (cordex, cmip7, ...)
        * identifiers: suffix.prefix, example cmip7.convert_celsius_to_kelvin
        * using synthethic data for testing

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

Next meeting: 8th June 2026

