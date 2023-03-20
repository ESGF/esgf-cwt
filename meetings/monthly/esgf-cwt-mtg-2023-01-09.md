# ESGF Compute Working Team Meeting - 2023-01-09

## Logistics

Where: Zoom

When:  09/01/2023

Who:  ESGF CWT:
- Ag Stephens (STFC CEDA)
- Carsten Ehbrecht (DKRZ)
- Sasha Ames (LLNL)
- David Huard (Ouranos)
- Alessandro Spinuso (KNMI)

## Actions

- [x] AS: Report recommencement of CWT meetings to ESGF XC
- [x] AS: Publish and share meeting minutes
- [x] AS: Share the roadmap with the XC and Slack team - https://github.com/ESGF/esgf-cwt/milestones
- [x] AS/CE: Draft the Terms of Reference then share: - https://github.com/ESGF/esgf-cwt/blob/main/documents/esgf-cwt-tor-2022-12-12.pdf

## Agenda


- Provenance (used by C4I - Notebooks)
- Gap between:
 - C3S
 - Required fully working ESGF Compute Node
 
Chat:

DH:- what about replicating between nodes?
 - if they only operate on local data, then if some nodes do not deploy Compute, then there is a risk that some ESGF data will not be accessible
SA: This is a risk, some nodes are unlikely to have resource to run a compute node - so some data would not be served.

SA: Intake catalog maintenance should be part of a data publication workflow.

DH: Intake doesn't scale well. 

CE: At DKRZ, it does take time to parse/load the intake catalogs. They act as a kind of documentation of what is available.

ASte: We probably need more experimentation regarding Intake.

SA: Globus team are going to ingest all of CMIP6 into their Globus database - which would sit on top of Elasticsearch on the backend. There is a discussion next week.

ASpi: Will they host in the Amazon cloud? 

SA: I think Globus is trying to address the zoning issue in the cloud - this is an important question for next week.

DH: What about including the ability to replicate data from remote sites as part of a roocs process? This could be managed to support small replications on-the-fly.

- [ ] AS/CE: think about roocs caching of remote data.
 - WPS should do that by default.
 - Could have a list of known services that can be replicated from. 

DH: Danger of replicating lots of data when it could be operated on at the remote node (that also happens to have a Compute Node running).

ASte: we could have a registry of Compute Nodes and they could send each other requests. Then the user would get back a list of URLs that might be at different sites.

- [ ] DH: Ask colleagues if they have thoughts on how this could be done.

CE: Would we need restrictions on user requests? 

ASte: Yes, we will need to manage access/limits somehow. Maybe using an API KEY.

ASpi: You would need to apply some access control and resource allocation, limitations and record metrics - through an API KEY.

SA: We may need limitations applied to search as well.

- [ ] AS/CE: Implement the API KEY from the start. We might be able to use Keycloak to provide this.

ASpi: for our Notebooks, we ask users to apply to request access. They apply for accounts and then Keycloak is used to manage their access.

SA: Keycloak can use a federated identity - e.g. GitHub, ORCID, Google etc. Note that Globus Auth knows about academic institutions. Some identities could be pre-approved for ESGF WPS access.

https://docs.google.com/presentation/d/1j5o0L9bKIfXyNo4gdJUNucbkcPWhGQsT6yhPjssmUr8/edit#slide=id.g1ca3d2c0a6f_0_6


