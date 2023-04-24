# ESGF Compute Working Team Meeting - 2023-03-20

## Logistics

Where: Zoom

When:  20/03/2023

Who:  ESGF CWT:
- Ag Stephens (STFC CEDA)
- Carsten Ehbrecht (DKRZ)
- Sasha Ames (LLNL)
- David Huard (Ouranos)
- Alessandro Spinuso 
- Ezequiel Cimadevilla (Instituto de Física de Cantabria (IFCA))

## Actions

- [x] AS/CE: Contact CMCC regarding `roocs` installation - **rook deployed over CMCC backend - meeting planned**
- [ ] AS/CE: think about `roocs` caching of remote data.
- [ ] AS/CE: Implement the API KEY/proxy from the start. We might be able to use Keycloak to provide this.
- [ ] DH: Keep CWT informed of developments regarding WMO + ESGF interactions.

## Agenda

1. Welcome and introductions

2. Actions and minutes from last meeting
- [ ] AS/CE: think about roocs caching of remote data. - **ongoing**
- [x] DH: Ask colleagues if they have thoughts on how caching of data could be managed within `roocs`.
- [ ] AS/CE: Implement the API KEY/proxy from the start. We might be able to use Keycloak to provide this. - **ongoing**

3. Roadmap:
- the team reviewed the Roadmap, at: [https://github.com/ESGF/esgf-cwt/issues/5](https://github.com/ESGF/esgf-cwt/milestones)

4. Discussion and questions

- CE: C3S roocs:
  - New version of the C3S Climate Data Store portal:
    - Will only interact with our `rook` WPS
  - There is a Slurm queue to handle heavy load:
    - already running at DKRZ
  - New IPCC Atlas data is being prepared:
    - Uses Intake catalog
    - Used to filter existing files _without operators_ (initially)
    - Download already works
    - Data is a subset of CMIP5 and CORDEX  
  - Support for Decadal CMIP6 data:
    - Each request returns 10 ensemble members
    - They get concatenated to add in a new coordinate variable (ensemble member)
    - Could use caching on the server-side

- ASpi: CMCC have deployed `roocs` - and attaching to Keycloak and Api Key
  - Paula and Marco have been working on this.
- [ ] AS/CE: Contact CMCC regarding `roocs` installation

- ASte: Proxy usage in the `roocs` stack:
  - showed issue ("Build a web-proxy into the deployment stack"): https://github.com/ESGF/esgf-cwt/issues/27
  - SA: the basic architecture looks okay. Regarding the _WPS Access Manager (WAM!)_, you might be able to re-use the prior knowledge in `Slurm` to deliver a _fair-share_ approach.
  - CE: `Twitcher` might be able to do some of this, but using existing components does make sense. When we get to fine-grained access, not sure if it could be controlled by `KeyCloak`.

- DH: CaSPAr plans
  - WMO has a recent initiative to update its holdings and sharing of data.
  - Looks similar to EGSF, see:
    - https://docs.wis2box.wis.wmo.int/en/latest/
  - It would be great to see high-level information-sharing and discussion
  - In Canada, one opportunity for building the bridge, would be the CaSPAr project:
    - combining WMO and ESGF components
  - Could be an opportunity to bring resources to ESGF
  - SA: WMO sponsors the WCRP, and the WCRP oversees ESGF - there should be better connections
- [ ] DH: Keep CWT informed of developments regarding WMO + ESGF interactions.

- Kerchunk thoughts/plans
  - See: https://docs.google.com/document/d/174yaaVnB-D9w_ne5ZkA9bdhmu1e0QjUA0U6Lj4156aE/edit#heading=h.7gv8m3mhigte

- Fixing data?
  - Apache Iceberg - could fit here. 

- Caching data from other ESGF nodes:
  - Weaver: already has functionality to query other nodes 
    - So Weaver can be a proxy, and/or can act as a WPS itself (if the WPS is dockerised)

5. Next steps:
   - add a “compute” section to this page on the ESGF site? https://esgf.github.io/projects.html
     - Fork github.com/ESGF/esgf.github.io/
     - commit updates, and create a PR for SA to merge
     - Can rewrite the entire CWT/Compute section.
     - DH: can review drafts (or draft)

6. AOB:
   - Next meeting:
     - Date: 17/04/2023 (avoiding 10th because UK holiday)
