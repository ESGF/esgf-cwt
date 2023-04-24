# ESGF Compute Working Team Meeting - 2023-04-24

## Logistics

Where: Zoom

When:  24/04/2023

Who:  ESGF CWT:
- Ag Stephens (STFC CEDA)
- Carsten Ehbrecht (DKRZ)
- Sasha Ames (LLNL)
- David Huard (Ouranos)
- Maxwell Grover (ANL)
- Aashish Chaudhary (Kitware)

## Actions

- [ ] AS/CE Consider Jenkins and other CI systems for potentially running the test suite
- [ ] AS/CE: add a “compute” section to this page on the ESGF site? https://esgf.github.io/projects.html
- [ ] AS/CE: think about `roocs` caching of remote data - **Ongoing - meeting on Friday**
- [ ] AS/CE: Implement the API KEY/proxy from the start. We might be able to use Keycloak to provide this. - **Ongoing - meeting on Friday**
- [ ] DH: Keep CWT informed of developments regarding WMO + ESGF interactions - **Ongoing**

## Agenda

1. Welcome and introductions

2. Actions and minutes from last meeting
- [x] AS/CE: Contact CMCC regarding `roocs` installation:
  - **rook deployed over CMCC backend - meeting planned**
- [ ] AS/CE: think about `roocs` caching of remote data:
  - **Ongoing - meeting on Friday - see diagram later**
- [ ] AS/CE: Implement the API KEY/proxy from the start. We might be able to use Keycloak to provide this:
  - **Ongoing - meeting on Friday**
- [ ] DH: Keep CWT informed of developments regarding WMO + ESGF interactions:
  - **Ongoing**

3. Roadmap and progress

Building a testing framework to support extensive testing of _lots of_ ESGF data:
- AS: We already have many unit tests for the `roocs` stack - but we want to build confidence in the code by continually adding more datasets to the test suite. We propose a generic testing structure that can be run across multiple sites, and reads real ESGF data from the local data node. Here is the plan:
  - https://github.com/roocs/rook/issues/222#issuecomment-1434511712
- MG: have you considered using Binder Bot to manage running the tests?
- AS: we generally intend to run locally (i.e. _on the node_, rather than in the cloud) so we probably want to run through a local suite
- SA: You could use Jenkins as a local service.
- DH: Using Jenkins locally to run all this would have the benefit of being simple to trigger, and to log the results.
- AS: we use GitLab CI on a local instance. 
- [ ] AS/CE Consider Jenkins and other CI systems for potentially running the test suite

Delegated processes and remote data caching in the `roocs` stack:
- AS: we have been discussing this issue, and came up with this diagram:
  - https://raw.githubusercontent.com/ESGF/esgf-cwt/main/drawio/esgf-cwt-delegation_v2.png
- DH: should the "multi-step process?" box happen at the start, and be generalised?
- [ ] AS/CE: Update the diagram to cope with the case of multiple inputs from multiple nodes - might need the multi-step at the start of the diagram
- SA: Could OpenDAP be used to GET data from a remote site? Or from a Kerchunk service?
- DH: might need different logic in the code if handling the streaming/non-streaming cases
- AC: Could you have a global cache within each site? E.g. capturing info per endpoint, from a hash of the inputs (including the endpoint).
- AS: Yes, that would be very sensible.
- AC: And you could add some policies for managing the cache
- AC: We are interested in STAC, have you looked at that?
- AS: Yes, we are working on some solutions, see: https://techblog.ceda.ac.uk/search/stac/indexing/2021/12/07/stac-update.html

4. Discussion and questions

AS Completed discussion notes from ESGF Hybrid meeting:
- Server-side computing: https://docs.google.com/document/d/15voNXoyrkZ1TdFnftieJPCXspwbSgpxB3ntIKbufAXk/edit?pli=1#heading=h.xdwp3qbdme0v
- Data Interfaces and Access: https://docs.google.com/document/d/1mu3_1TDHJr9aqvEba9VWGAXO_3Nm5WESZxj2LtOjbZM/edit?pli=1#heading=h.xdwp3qbdme0v
- AS: my conclusion is:
  - Cloud-optimised approach AND remote processing ARE BOTH REQUIRED AND USEFUL. 

Kerchunk thoughts/plans
- AS: we are planning to get some community engagement on Kerchunk, we have been doing experiments at CEDA and my colleague will publish a blog on some of our findings/issues.
- ESGF Kerchunk google doc: https://docs.google.com/document/d/174yaaVnB-D9w_ne5ZkA9bdhmu1e0QjUA0U6Lj4156aE/edit#heading=h.7gv8m3mhigte
- MG: Would be great to revisit and work together over ESGF. Note that Deepak at NCAR has put together a post about using pre-aggregation:

https://ncar.github.io/esds/posts/2023/kerchunk-mom6/

MG: Some work has been done for using Parquet and other formats for Kerchunk.

- [ ] AS: look at parquet for Kerchunk format



5. Next steps:
- add a “compute” section to this page on the ESGF site? https://esgf.github.io/projects.html
  - Fork github.com/ESGF/esgf.github.io/
  - commit updates, and create a PR for SA to merge
  - Can rewrite the entire CWT/Compute section.
  - DH: can review drafts (or draft)

6. AOB:

DH Has some funding to support to work on the CWT

- [ ] AS organise meeting with DH

MG: For AGU, supporting short-course session.

SA: Forrest has drafted a google doc for short courses for AGU. If CWT Compute Node is working - we could include it.

SA Regarding Keycloak, it looks like [EGI-Checkin](https://www.egi.eu/service/check-in/) and [Globus-Auth](https://www.globus.org/platform/services/auth) might be replacing Keycloak for LLNL.
   - Next meeting:
     - Date: 15/05/2023 (avoiding 8th because UK holiday)
