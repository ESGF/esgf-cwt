# ESGF Compute Working Team Meeting - 2023-12-11


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  11/12/2023 

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Maxwell Grover (ANL)
- Carsten Ehbrecht (DKRZ)
- David Huard (Ouranos)
- Ezequiel Cimadevilla (Uni Can)
- Martin Schupfner (DKRZ)
- Nils Hempelmann (OGC)
- Paola Nassisi (CMCC)


## Agenda

### 1. Welcome and introductions

### 2. Actions and minutes from last meeting

- [ ] Max test running rook on the US side - Ansible (ongoing)
- [ ] Neil follow up with CEDA group about STAC + elasticsearch process
- [ ] DH: Set up a mtg with Tom Kralidis and SA, to discuss WMO WIS - in November.
    - David working on this, will update at the next meeting


### 3. Discussion

Round Table:

Max: 

- working on the Ansible deployment ... on ubuntu ... but found some issues.


Nils:

- innovation week ... Tom Landry provided contact
- discussions: bringing services together ... copernicus ... noaa ... nasa 
- motivation: why should they change their systems
- OGC: better arguments to have fair climate services
- upcoming pilot: desaster and recovery service
- Copernicus services will jump in for the second phase

CE:

- new rook and clisops release with regridding operator. 
- example notebook with regrid operator: 
https://nbviewer.org/github/roocs/rooki/blob/master/notebooks/demo/demo-rooki-regrid-cmip6.ipynb 
- Tomorrow at 14:00 (Hamburg time) there will be a short meeting with the ESMValTool people. Ag will join. We want to work on a common solution for providing fixes to climate model data.  
- Copernicus: we will make the ATLAS v1 data available via Copericus CDS. Needs to done before xmas. 
- .. ATLAS v0 is already available:
https://cds.climate.copernicus.eu/cdsapp#!/dataset/projections-climate-atlas 

Ezequiel:

- pangeo meeting: how costly to move data to the cloud?
- ... very costly
- David: make a show case
- binder links:
https://github.com/zequihg50/2023-esgf-virtual-aggregation#rationale

David:

- my college is working on spatial aggregation

Martin:

- PR for xesmf ... for convervative regriding.

Paola:

- integrated the "rook wps" (without clisops ... just the interface) in our system at CMCC.


### 4. Next steps:



### 5. AOB:

Next meeting: 8th January 2024




 
 
 
 
 
