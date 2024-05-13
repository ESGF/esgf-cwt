# ESGF Compute Working Team Meeting - 2024-05-13


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  13/05/2024

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)
- Nils Hempelmann (OGC)
- David Huard (Ouranos)
- Ezequiel Cimadevilla (Uni Can)
- William Tucker (CEDA/STFC)
- Ben Coalson (ORNL)
- Forrest Hoffman (ORNL)


## Agenda

### 1. Welcome and introductions

### 2. Actions and minutes from last meeting

- [ ] Max + Carsten: work on docker deployment
- [ ] Carsten: add wiki page for presenters
- [ ] Max test running rook on the US side - Ansible (ongoing)
- [ ] Neil follow up with CEDA group about STAC + elasticsearch process
- [ ] DH+Sasha+Max: Set up a mtg with Tom Kralidis to discuss WMO WIS - at ESGF F2F in April? or at least in CWT

### 3. Presentation (optional)


See list of presentations in issue https://github.com/ESGF/esgf-cwt/issues/35.


### 4. Discussion

#### Round Table

**Nils** 

* organizing FOSS4G/OGC in Tatu, Estonia. 
* Copernicus C3S has focus on energy and health thematic. 
* Possbile to take part online. 
* David supported keynote abstract.
* New OGC Director: https://www.linkedin.com/in/peterrabley/ 

The OGC Testbed-20 Call for Participation (CFP) just went live!

https://www.ogc.org/initiatives/ogc-testbed-20/

The testbed will feature tasks on:

Integrity, Provenance, and Trust (IPT)
GEOINT Imagery Media for ISR (GIMI)
Advancements on GeoDataCubes
High-Performance Geospatial Computing Optimized Formats

Responses to the CFP are due by 10 June 2024, @11:59 PM AoE. A Bidders Q&A Webinar will be held on 24 May, 10:00-11:00

**Max** 

* work on containerizing WPS services. 
* kerchunk with globus work in progress https://github.com/mgrover1/kerchunk-esgf-wip
* attended globus week.

**David** 

PR for polygon averaging released. Let me know.

**Forrest** 

* good meeting at ESGF F2F. 
* Index + message queue top priority. 

**Ezequiel** 

no updates

**Ben** 

no updates

**Carsten**

using ansilbe deployment for WPS within the CLINT project


#### Talk about Docker deployment

Ben:
I think the helm charts would fill a similar role to the docker compose in that it facilitates deploying into various kubernetes environments like William was saying

Max:
the WPS containerization repo: https://code.ornl.gov/esgf/wps

David:
* deploy with docker-compose in production:L https://github.com/bird-house/birdhouse-deploy
* Bird in production: https://github.com/bird-house/finch
* build rook image on docker-hub

### 5. Next steps:

Max + Carsten have a look at the docker-compose deployment of Ouranos and try to adapt it for rook WPS.

### 6. AOB:

Next meeting: 10th June 2024

