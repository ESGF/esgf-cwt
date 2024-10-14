# ESGF Compute Working Team Meeting - 2024-10-14


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  14/10/2024

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)
- David Huard (Ouranos)
- Nils Hempelmann (OGC)
- Zach Price (ORNL)
- Forrest Hoffman (ORNL)
- Ben Coalson (ORNL)
- Alessandro Spinuso (KNMI)

## Agenda

### 1. Welcome and introductions

### 2. Actions and minutes from last meeting

- [ ] Update calendar entry
- [ ] Carsten: prepare new bird "Nandu" with pygeoapi on bird-house
- [ ] Max + Carsten: work on docker deployment
- [ ] Carsten: add wiki page for presenters
- [ ] Neil follow up with CEDA group about STAC + elasticsearch process

### 3. Presentation (optional)

See list of presentations in issue https://github.com/ESGF/esgf-cwt/issues/35.

### 4. Discussion

#### Round Table

Nils:
- wrap up of coding-sprint of CLINT project at Bonn
    - https://www.ogc.org/ogc-events/2024-climate-services-code-sprint/
    - worked quite well :)
    - connected now with the developers directly
    - first level of integration of wps CLINT AI services into copernicus services (e.a. wekeo)
    - https://www.wekeo.eu/
    - should clean birdhouse documents
    - Zoo project with Gerald was also present (ogcapi-processes, CWL, docker, kubernetes)
    - should move to pygeoapi which can also be integreated into Zoo
- ECMWF sponsers the next OGC climate pilot

David:
- desire to move our finch WPS to pygeoapi ... in the next 6 months
- created stac catalogs for CORDEX data
    - PR create to stac item from CORDEX-CV: https://github.com/WCRP-CORDEX/cordex-cmip6-cv/pull/188

Zach:
- work also on STAC
- https://github.com/ESGF/ESGF-Playground
- Rook/WPS is working
- working on a new installation

Forrest:
- F2F meeting at UK
- registration form: 
https://docs.google.com/forms/d/e/1FAIpQLScPNbLqQ90PRgHBhPUQQRfvTrVvODVm_q2TXNDpNsQuwDRK_g/viewform?usp=sf_link
- look at the core architecture
- come up with a timeline in middle of 2025
- with synced indexes

Alessandro:
- outcome of WMO workshop:
https://community.wmo.int/en/meetings/sg-fit-workshop-2024
- OGC reference architecture shown on days 2 + 3
- links are broken ... will send the documents on mailing-list
- the recordings are working
- associated member at WMO

Carsten:
- TODO: update CWT calendar entry
- attended CLINT coding spring at ECMWF/Bonn: 
- move to pygeoapi? could also be integrated with CWL and Zoo.
- join F2F in UK beginning of November


### 5. Next steps:

William likes to test the current docker deployment.

Work on pygeopi and STAC.

### 6. AOB:

Next meeting: 11th November 2024

