# ESGF Compute Working Team Meeting - 2026-01-12


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  12/01/2026

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)
- David Huard (Ouranos)
- Zach Price (ORNL)
- Alessandro (KNMI)

## Agenda

### 1. Welcome and introductions

### 2. Actions and minutes from last meeting

- [ ] Carsten + David: work on pygeoapi + STAC
- [ ] Carsten: work on docker deployment

### 3. Presentation (optional)

See list of presentations in issue https://github.com/ESGF/esgf-cwt/issues/35.

### 4. Discussion

#### Round Table

Carsten:
* made a new release of rook with regrid operator.

David:
* TODO: please write a data paper on rook + clisops. ask Ag ... etc
* I like to mention Rook/ESGF2 in the cmip7 ipcc report

Alessandro:
* there are some upcoming deliverables that can help for the ipcc report
* how will the WPS be made available via the stac catalog? (still an open point!)
* how is the stac catalog orgainzed? (stac item = dataset, stac assets = files, globus end points and for aggregated access zarr or kerchunk)

Zach:
* There is an aggregation extension for stac:
    * https://github.com/stac-api-extensions/aggregation
    * https://api.stac.esgf.ceda.ac.uk/collections/CMIP6/aggregate?aggregations=cmip6_source_id_frequency,cmip6_table_id_frequency 
    * https://api.stac.esgf.ceda.ac.uk/collections/CMIP6/aggregations
* there might be something available to search on files (assets, need to ask Rhys from CEDA).


### 5. Next steps:

* Work on pygeopi and STAC. 
* Need a new cookiecutter and birdy. 
* Work on docker deployment. 
* Integrate with S3 storage. 
* Need a production ready (better queue) pygeoapi.
* Work on prov db for Rook WPS

### 6. AOB:

Next meeting: 9th February 2026

