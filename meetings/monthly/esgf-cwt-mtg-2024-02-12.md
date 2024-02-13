# ESGF Compute Working Team Meeting - 2024-02-12


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  12/02/2024

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Maxwell Grover (ANL)
- Carsten Ehbrecht (DKRZ)
- David Huard (Ouranos)
- Charles Gauthier (Ouranos)
- Martin Schupfner (DKRZ)
- Fabian Wachsmann (DKRZ)
- Katharina Berger (DKRZ)
- Nils Hempelmann (OGC)
- Alessandra Nuzzo (CMCC)
- Sasha Ames (LLNL)
- Zach Price (ORNL)
- Ben Coalson (ORNL)
- Alessandro Spinuso (KNMI)

## Agenda

### 1. Welcome and introductions

### 2. Actions and minutes from last meeting

- [ ] Max test running rook on the US side - Ansible (ongoing)
- [ ] Neil follow up with CEDA group about STAC + elasticsearch process
- [ ] DH+Sasha+Max: Set up a mtg with Tom Kralidis to discuss WMO WIS - at ESGF F2F in April? or at least in CWT


### 3. Discussion

Round Table:

Max: 

- ESGF F2F in Washington 23.4-26.4 (?) ... hard to get a hotel there ... 
- scipy conference in US: https://scipy.org/
- got pywps deployment running with ansible ... talk about it next time


Nils:

- working on OGC demonstrator ... David knows
- OGC climate pilot ... got new sponsors
- foss4g Europe in Estonia in July ... OGC 2 day event: 

https://2024.europe.foss4g.org/


Sasha:

- no updates


David:

- bringing togther OSGEO and WMO
- TODO: Tom Kralidis from WMO ... could talk at ESGF F2F ... or to us


Charles:

- PR to clisops with `average_shape` operator merged
- TODO: PR daops needs review


Alessandro:

- no updates
- worked on proposal for provenance


Alessandra:

- no updates


CE:

- new Rook WPS release for Copernicus with support for subsetting of Atlas v1 data. 
- will be integrated in the next weeks in the Climate Data Store.
- we have to apply some fixes to the Atlas data to make same "usable" (to write them with netcdf):
https://github.com/roocs/clisops/issues/317
- Example notebook with rooki:
https://nbviewer.org/github/roocs/rooki/blob/master/notebooks/demo/demo-rooki-c3s-cica-atlas.ipynb 


Fabi:

- talk about xpublish
- xpulish-plugins for intake and opendap available
- chunk-based
- not used for replication
- zarr endpoint
- can compress data on access
- use holoviews in a notebook app to visualize data with time-slider ... like ncview
- serves kerchunked files: 1 GB memory for 100 TB files
- demo VM at DKRZ: 16 CPUs, 64 GB, limited to 4 parallel requests
- [xpublish slides by Fabi](https://docs.google.com/presentation/d/1scqkdz84SDocLqs3pV-L2okmfyHdiARMn6eb0Mae9Ik/edit#slide=id.p1)
- https://eerie.cloud.dkrz.de/datasets
- https://gitlab.dkrz.de/data-infrastructure-services/eerie-io/-/blob/main/xpublish/host_dynamic_dsets.py?ref_type=heads
- https://swift.dkrz.de/v1/dkrz_7fa6baba-db43-4d12-a295-8e3ebb1a01ed/apps/eerie-cloud_view-and-access.htm
- https://swift.dkrz.de/v1/dkrz_7fa6baba-db43-4d12-a295-8e3ebb1a01ed/apps/eerie-cloud_gr025_interactive-animation.html


### 4. Next steps:



### 5. AOB:

Next meeting: 11th March 2024




 
 
 
 
 
