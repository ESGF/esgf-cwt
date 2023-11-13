# ESGF Compute Working Team Meeting - 2023-10-16


## Logistics

Where: zoom

When:  16/10/2023

Who:  ESGF CWT:

- Ag Stephens (STFC CEDA)
- Carsten Ehbrecht (DKRZ)
- Sasha Ames (LLNL)
- David Huard (Ouranos)
- Ezequiel Cimadevilla (Uni Can)
- Alessandro Spinuso (KNMI)
- Alessandra Nuzzo (CMCC)
- Charles Gauthier (Ouranos)
- Prashanth Dwarakanath Roa (LIU)
- Nils Hempelmann (OGC)

## Actions

- [ ] CE send out new invite
- [ ] DH: Set up a mtg with Tom Kralidis and SA, to discuss WMO WIS - in November.

## Agenda

### 1. Welcome and introductions

### 2. Actions and minutes from last meeting

Prashanth Dwarakanath Roa (LIU): 
- Take a look at CMOR Fixer - developed by KNMI - lots of fixing
- [ ] AS/SA to look at CMOR Fixer
  - https://github.com/EC-Earth/cmor-fixer
  - it appends a line to headers noting that it has been processed

Kerchunk / Parquet
- Ezeq: generating KC takes a long time - bit task
- [ ] Talk to Ezequiel about chunking limitations

- MG:
 - have you thought of syncing the Reference File Generation with Zarr/PANGEO-FORGE
 

### 3. Discussion

Nils:
 Proj Mngr at OGC, focusing on climate data and climate projects/services.
 Main focus of the work is setting up climate and climate/disaster resilience pilots.
 Keen on WPS and OGC API Processes
 
CG: working at Ouranos, will be to embed polygon averaging into "roocs":
- to allow sending in a Shapefile to define the polygon and then returning the subset within it
- minimum working implementation
 
ASpi: can put us in touch with somebody aon the cmor-fixeer team.
  

SA: update to ESGF Search schema:
 - change the way replication works

OGC Update from NH:
1. OGC Innovation Days in Washington in December (4th-6th):
 - focus on data processing for climate and disaster risk mngmt
 - in-person meeting only
2. Upcoming climate pilot:
 - sponsored by ECMWF C3S
 - interoperability gap-analysis for the CDS and ADS (C3S)
 - "roocs" could be in scope

DH:
- posted in Slack channel
- There is a THREDDS to STAC harvester
- [ ] Need to explore this: https://ds2stac.readthedocs.io/en/latest/

ASpi:
- moving to EGI Check-in next year for ESGF
- can "roocs" move to that?
 - SA: we should be able to leverage nginx middleware routing to manage this, with EGI Check-in.

Aspi:
- will be participating a meeting with WMO on climate services provenance requirements
  - lineage, provenance and updates to data
  - demonstrating "roocs"

SA: 
- there is an `intake-esgf` cataloguing package under development:
  - https://github.com/nocollier/intake-esgf/


ArrayLake:
https://discourse.pangeo.io/t/esip-cloud-computing-cluster-oct-30-arraylake-a-cloud-native-data-lake-platform-for-earth-system-science/3753


### 4. Next steps:


### 5. AOB:

Next meeting: 13th November 2023




 
 
 
 
 