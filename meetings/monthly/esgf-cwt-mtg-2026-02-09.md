# ESGF Compute Working Team Meeting - 2026-02-09


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  09/02/2026

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)
- Nils
- David Huard (Ouranos)
- Zach Price (ORNL)
- Alessandro (KNMI)

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

Carsten:
* kick-off meeting for Copernicus. Integrate CORDEX, CMIP7 etc. Work on QA/QC (ioos compliance checker) which is also used for ESGF2.
* next try on fixing library. Together with Ag (STFC/CEDA). 

Nils:
* organizing copernicus meeting ... in-person event with broadcast for questions
    * https://climate.copernicus.eu/9th-c3s-general-assembly
    * ... the future developement of CDS
    * ... stronger network with other services
    * in June in Budapest
* clint is running out
    * very successful project ... fulfilled the promises
    * cyclone tracking ... now in the CDS ... not official yet
    * Here is the Cyclon Activity application: 
https://apps.climate.copernicus.eu/earthkit-dataset-viewer/?dataset=clint

Alessandro:
* Futura and ines-rise will be funded!
* coordinated by Anna, CMCC
* DKRZ got quite some resources in it
* how about the WPS will evolve in ESGF2?
* infra part and a research component
* support IPCC
* support ESGF2 ... east (UK)
* isenes-rise ... Plan B ... keep up the data nodes for next 3-4 years
* David: what does it change for the rest of the world?
* A: the US (globus) and UK (egi-checkin, es) ESGF2 are different ... but use the same interface (STAC)
* Zach: 
* A: we have data-challenges to test the interfaces

Zach:
* still working how to integrate WPS ... eg STAC integration
* metagrid: 
    * update to use STAC catalog

David:
* editor for IPCC ... waiting for cmip7 data  ... deadline already in summer
* francis works on CLI mapper to ogc-api ... not using pygeoapi
* A: do you use CWL? D: yes
* A: it is done in-memory? D: I look up the code: https://github.com/bird-house/goldfinch



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

Next meeting: 9th March 2026

