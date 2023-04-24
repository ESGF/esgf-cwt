# ESGF Compute Working Team Meeting - 2023-04-24

## Logistics

Where: Zoom

When:  24/04/2023

Who:  ESGF CWT:
- Ag Stephens (STFC CEDA)
- Carsten Ehbrecht (DKRZ)
- Sasha Ames (LLNL)
- David Huard (Ouranos)
- Alessandro Spinuso 
- Ezequiel Cimadevilla (Instituto de Física de Cantabria (IFCA))

## Actions

- [ ] AS: add a “compute” section to this page on the ESGF site? https://esgf.github.io/projects.html
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

- Unit testing:
  - Alan at CEDA, starting to look at generic testing structure:
    - https://github.com/roocs/rook/issues/222#issuecomment-1434511712

- Working with remote `rooks` and data:
  - Ag and Carsten discussed:
    - https://raw.githubusercontent.com/ESGF/esgf-cwt/main/drawio/esgf-cwt-delegation_v2.png

- Ag Completed discussion notes from ESGF Hybrid meeting:
  - Server-side computing: 
  - Data Interfaces and Access:
  - Conclusion?
    - Cloud-optimised approach AND remote processing ARE A GOOD COMBINATION???!!! 

4. Discussion and questions




- Kerchunk thoughts/plans
  - See: https://docs.google.com/document/d/174yaaVnB-D9w_ne5ZkA9bdhmu1e0QjUA0U6Lj4156aE/edit#heading=h.7gv8m3mhigte




5. Next steps:
   - add a “compute” section to this page on the ESGF site? https://esgf.github.io/projects.html
     - Fork github.com/ESGF/esgf.github.io/
     - commit updates, and create a PR for SA to merge
     - Can rewrite the entire CWT/Compute section.
     - DH: can review drafts (or draft)

6. AOB:
   - Next meeting:
     - Date: 15/05/2023 (avoiding 8th because UK holiday)
