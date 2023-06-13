# ESGF Compute Working Team Meeting - 2023-06-12

## Logistics

Where: Zoom

When:  12/06/2023

Who:  ESGF CWT:
- Ag Stephens (STFC CEDA)
- Carsten Ehbrecht (DKRZ)
- Sasha Ames (LLNL)
- David Huard (Ouranos)
- Ezequiel Cimadevilla (Uni Can)
- Alessandro Spinuso (KNMI)
- Alessandra Nuzzo (CMCC)
- Forrest Hoffman (ORNL)

## Actions

- [ ] ASte/CE Consider Jenkins and other CI systems for potentially running the test suite - **ongoing**
- [ ] ASte: look at parquet as Kerchunk format - does it help us with large file problems - **ongoing**
- [ ] ASte/CE: think about `roocs` caching of remote data - **Ongoing - meeting on Friday**
- [ ] ASte/CE: Update the diagram to cope with the case of multiple inputs from multiple nodes - might need the multi-step at the start of the diagram - **ongoing**
- [ ] ASte/CE: Implement the API KEY/proxy from the start. We might be able to use Keycloak to provide this. - **Ongoing - meeting on Friday**
- [ ] DH: Keep CWT informed of developments regarding WMO + ESGF interactions - **Ongoing**

## Agenda

1. Welcome and introductions

2. Actions and minutes from last meeting

- [ ] ASte/CE Consider Jenkins and other CI systems for potentially running the test suite - **ongoing**
- [ ] ASte: look at parquet as Kerchunk format - does it help us with large file problems - **ongoing**
- [x] ASte organise meeting with DH to discuss supporting the CWT - **Done**
- [x] ASte/CE: Update the ESGF site with new details about the CWT and compute: https://esgf.github.io - **Done**
  - It was discussed that the ESGF website might get an overhaul during the ESGF 2.0 project - but currently a low priority.

- [ ] ASte/CE: think about `roocs` caching of remote data - **ongoing**
- [ ] ASte/CE: Update the diagram to cope with the case of multiple inputs from multiple nodes - might need the multi-step at the start of the diagram - **ongoing**
- [ ] ASte/CE: Implement the API KEY/proxy from the start. We might be able to use Keycloak to provide this. - **ongoing**
- [ ] DH: Keep CWT informed of developments regarding WMO + ESGF interactions - **ongoing**

3. Discussion

Kerchunk, Zarr etc:
- ASte: I looked briefly into whether Parquet would be a better Kerchunk format than JSON. It doesn't look like it will create
      smaller files than using `zstd`.
- DH: The Zarr version 3 spec might solve this problem.

Ouranos work on CWT:
- DH:
  - we have funding to direct some effort on ESGF-CWT
  - an intern will be to embed polygon averaging into "roocs"
    - to allow sending in a Shapefile to define the polygon and then returning the subset within it

Interactions with the WMO regarding WIS:
- DH: We had a meeting with Tom Kralidis, to discuss WMO WIS system. Uses a federated system around the globe - like ESGF.
      They use a pub/sub model and global caches. There might be opportunities to consider interactions with ESGF. 
      WMO is renewing its digital architecture to share forecast and obs data - some overlap with ESGF.
- ASpi: we have seen the WMO WIS but there is no plan to implement. We are also busy with interactions with the European Weather Cloud - which is also setting up a federation of services/systems.

DH: there seems to be less strictness regarding the backend. Just HTTP pointers to file download systems.

4. Discussion and questions

AS Completed discussion notes from ESGF Hybrid meeting:
- Server-side computing: https://docs.google.com/document/d/15voNXoyrkZ1TdFnftieJPCXspwbSgpxB3ntIKbufAXk/edit?pli=1#heading=h.xdwp3qbdme0v
- Data Interfaces and Access: https://docs.google.com/document/d/1mu3_1TDHJr9aqvEba9VWGAXO_3Nm5WESZxj2LtOjbZM/edit?pli=1#heading=h.xdwp3qbdme0v
- AS: my conclusion is:
  - Cloud-optimised approach AND remote processing ARE BOTH REQUIRED AND USEFUL. 

Kerchunk thoughts/plans:
- AS: we are planning to get some community engagement on Kerchunk, we have been doing experiments at CEDA and my colleague will publish a blog on some of our findings/issues.
- ESGF Kerchunk google doc: https://docs.google.com/document/d/174yaaVnB-D9w_ne5ZkA9bdhmu1e0QjUA0U6Lj4156aE/edit#heading=h.7gv8m3mhigte
- MG: Would be great to revisit and work together over ESGF. Note that Deepak at NCAR has put together a post about using pre-aggregation: https://ncar.github.io/esds/posts/2023/kerchunk-mom6/
MG: Some work has been done for using Parquet and other formats for Kerchunk.
- [ ] AS: look at parquet as Kerchunk format - does it help us with large file problems.

5. Next steps:
- [ ] AS: add a “compute” section to this page on the ESGF site? https://esgf.github.io/projects.html
  - Fork github.com/ESGF/esgf.github.io/
  - commit updates, and create a PR for SA to merge
  - Can rewrite the entire CWT/Compute section.
  - DH: can review drafts (or draft)

6. AOB:
- DH Has some funding to support to work on the CWT
  - [ ] AS organise meeting with DH to discuss supporting the CWT
- MG: For AGU, supporting short-course session.
- SA: Forrest has drafted a google doc for short courses for AGU. If CWT Compute Node is working - we could include it.
- SA: Regarding Keycloak, it looks like [EGI-Checkin](https://www.egi.eu/service/check-in/) and [Globus-Auth](https://www.globus.org/platform/services/auth) might be replacing Keycloak for LLNL.
- Next meeting:
  - Date: 15/05/2023 (avoiding 8th because UK holiday)
