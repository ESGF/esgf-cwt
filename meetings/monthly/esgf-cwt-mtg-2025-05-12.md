# ESGF Compute Working Team Meeting - 2025-05-12


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  12/05/2025

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)
- David Huard (Ouranos)
- Alessandro Spinuso (KNMI)


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
* Seneca wants to use S3 storage to provide ESGF data (IRISC project). How can this be integrated with Rook/WPS and ESGF2?
* David: 
    * either use zarr with s3
    * or upload complete netcdf files to S3 and provide a kerchunk file to access these files as chunks.


Alessandro:
* ESGF status: https://github.com/ESGF/esgf-roadmap/tree/main/status
* PROV namespace: we need to use consistent namespace URLs.
* Please keep us informed about the transition to the new ESGF2 with STAC. Many Apps lely on the current ESGS-search (sorl ... mot stac)!

David:
* the pygeoapi project has an example for accessing files on S3 storage.


### 5. Next steps:

Work on pygeopi and STAC. Need a new cookiecutter and birdy. Work on docker deployment. Integrate with S3 storage.

### 6. AOB:

Next meeting: 14th July 2025

