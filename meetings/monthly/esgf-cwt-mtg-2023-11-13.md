# ESGF Compute Working Team Meeting - 2023-11-13


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  13/11/2023 

* 16:15 - 17:00 Hamburg
* 15:15 - 16:00 UTC
* 10:15 - 11:00 Montreal
* 07:15 - 08:00 San Francisco

Who:  ESGF CWT:

- Maxwell Grover (ANL)
- Neil Massey (STFC CEDA)
- Carsten Ehbrecht (DKRZ)
- Martin Schupfner (DKRZ)
- Sasha Ames (LLNL)
- David Huard (Ouranos)
- Ezequiel Cimadevilla (Uni Can)
- Charles Gauthier (Ouranos)
- Nils Hempelmann (OGC)
- Christian Pagé (CERFACS)
- Forrest Hoffman (ORNL)
- Ben Coalson (ORNL)

## Actions

- [ ] One.
- [ ] Two.

## Agenda

### 1. Welcome and introductions

### 2. Actions and minutes from last meeting

- [x] CE send out new invite
- [ ] DH: Set up a mtg with Tom Kralidis and SA, to discuss WMO WIS - in November.
    - David working on this, will update at the next meeting


### 3. Discussion

CE: 
* who is using the ioos compliance checker?
https://github.com/ioos/compliance-checker
    - Tool for checking for cf-compliance
    - Similar to pytest, can check for different specs
* WPS with rook
    - New updates, not regridding yet, but it has new averaging functionality
    - [Demo Notebook](https://nbviewer.org/github/roocs/rooki/blob/master/notebooks/demo/demo-rooki-concat-with-average-cmip6-decadal.ipynb)


Discussion:
* What are the requirements for integration with the ESGF stack? What do node managers expect to implement?
   - Not sure where this stands...
   - Max - testing this on the US side
   - Make sure that there are clear setup requirements, some containerized method
     - Two ways - **Ansible playbook** + helm chart
   - Question about key priorities within the stack
     - esdoc - not clear here

### Updates

Max G.:
* working on CMIP6 cookbook https://github.com/ProjectPythia/cmip6-cookbook

Charles G. 
* adding tests for rook, daops and clisops, testing the stack

Nils: 
* working with climate intelligence project, WPS services, enhancing AI for climate, had a coding sprint in Hamburg last month 
* New climate + disaster call for OGC (supported by ECMWF), call for participation, kickoff in January, workshop later next year
    - Question about opportunity for Obs4MIPs - not included right now, but would be nice to see this! 
* OGC member meeting in June 2024, in Montreal
* [Call for participation call, in collaboration with NASA + other folks](https://www.ogc.org/initiatives/open-science/)
* [OGC Innovation Days in December](https://www.ogc.org/ogc-events/2023-ogc-innovation-days-and-climate-and-disaster-workshop/)


Neil M.: 
* CEDA's rep on these meetings, still spinning up, involved in STAC for ESGF (still spinning up)
* Plan to follow up about sharing STAC setup with ESGF (have their own custom version of STAC)
* Current plan is import existing SOLR catalog into globus search (elastic search)
* Question about searching across the federation - still a priority, would be good to have within the global index

Ezequiel: 
* checking out the CMIP6 cookbook

Sasha: 
* Jason is working on benchmarks for direct file open vs. Zarr/kerchunk access, aggregated local opendap

### 4. Next steps:

- [ ] Max test running rook on the US side - Ansible
- [ ] Neil follow up with CEDA group about STAC + elasticsearch process


### 5. AOB:

Next meeting: 11th December 2023




 
 
 
 
 
