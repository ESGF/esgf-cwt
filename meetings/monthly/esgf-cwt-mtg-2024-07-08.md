# ESGF Compute Working Team Meeting - 2024-07-08


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  08/07/2024

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)
- David Huard (Ouranos)
- William Tucker (CEDA/STFC)
- Zach Price (ORNL)
- Forrest Hoffman (ORNL)
- Nils Hempelmann (OGC)
- Alessandro Spinuso (KNMI)


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

#### Max about ESGF notebooks using Rook WPS 

Last week at the Project Pythia hackathon, students worked on new notebooks for the ESGF cookbook
* Remotely Computing ENSO + Regridding + Calculating Non-Linearity: https://projectpythia.org/esgf-cookbook/notebooks/rooki_enso_nonlinear.html
* Remotely regridding + comparing the output from models locally: https://projectpythia.org/esgf-cookbook/notebooks/ex-regrid-plot.html
* Searching the Globus-Hosted Index and Computing with Rooki: https://projectpythia.org/esgf-cookbook/notebooks/use-intake-esgf-with-rooki.html

They also highlighted the need for an example searching for datasets using intake-esgf, and feeding those datasets into rooki
https://projectpythia.org/esgf-cookbook/notebooks/use-intake-esgf-with-rooki.html

Be on the lookout for some PRs to rooki to expand the documentation, especially chaining operations together 

I would be happy to present on this at our next CWT meeting.

#### Notes

Skipped the presentation today ... maybe next time when Max is available.


### 4. Discussion

#### Round Table

David: 
* build docker image from the repo

Nils: 
* CLINT workshop in 7th-9th of October 2024. ... open for everybody. Target how to deploy birds in the clint infrastructure.
* https://docs.google.com/document/d/1t_pJj1lXlC4ufJu9aCJzMRlvD06f31bq0KdfLC0gD7w/edit#heading=h.dd64qpd7kjb5

William:
* no updates

Zach:
* deployed Rook ... found no technical issues. used a docker deployment. with cmip6 ...
* https://esgf-wps.apps.onyx.ccs.ornl.gov/wps?service=WPS&request=getcapabilities
* https://code.ornl.gov/esgf/wps/-/blob/main/helm/values.yaml?ref_type=heads#L9-51
* https://code.ornl.gov/esgf/wps

Forrest:
* no updates

Alessandro:
* next year we have new project ... national  ... knmi will implement ogc services ... map services (adaguc) ... cloud based resources ...
* ... looking for use-cases
* https://developer.dataplatform.knmi.nl/edr-api
* https://github.com/xpublish-community/xpublish-edr
* https://docs.pygeoapi.io/en/stable/data-publishing/ogcapi-edr.html

Carsten:
* worked on docker deployment of rook: 
* https://github.com/roocs/rook/tree/dev-docker

#### Talked about docker deployment

Carsten: 
* How do customize the docker deployment ... especially for the roocs.ini config?

William:
* In ESGF we use Ansible and Helm for this.
* The ansible part of the Rook deploment can go into the ESGF repo
* the dockerfile and docker-compose can stay in the Rook repo.
* having an entrypoint.sh script to update the roocs.ini template on start-up is finde ... but don't spend too much time on it.

Zach:
* it is common practise to use entrypoint.sh in dockerfiles

### 5. Next steps:

William likes to test the current docker deployment.

### 6. AOB:

Next meeting: 12th August 2024

