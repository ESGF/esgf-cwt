# ESGF Compute Working Team Meeting - 2022-12-12

## Logistics

Where: Zoom

When:  12/12/2022

Who:  ESGF CWT:
- Ag Stephens (STFC CEDA)
- Carsten Ehbrecht (DKRZ)
- Sasha Ames (LLNL)
- David Huard (Ouranos)
- Katharina Berger (DKRZ)
- Rob Jacob (ANL)
- Ezequiel Cimadevilla (Instituto de Física de Cantabria (IFCA))

## Actions

- [x] AS: Report recommencement of CWT meetings to ESGF XC
- [x] AS: Publish and share meeting minutes
- [x] AS: Share the roadmap with the XC and Slack team - https://github.com/ESGF/esgf-cwt/milestones
- [x] AS/CE: Draft the Terms of Reference then share: - https://github.com/ESGF/esgf-cwt/blob/main/documents/esgf-cwt-tor-2022-12-12.pdf

## Agenda

This meeting is a change from the usual as we will be inviting people from outside the team to contribute to a wider discussion around compute services. We will be opening up the agenda to allow different groups to:
- share their work/experiences
- exchange ideas
- make suggestions about future directions

People may want to bring along ideas related to new technologies/standards/projects, such as:
- PANGEO
- OGC Web Services
- OGC API - Processes
- CLINT - Climate Intelligence
- Integration with other tools/domains
- Jupyter Notebooks
- Docker, Singularity, Kubernetes etc
- Other tools not yet considered

### Discussion

SA: heard of **GeoServer** as an alternative WPS platform for ESGF2.
- could it work for us, e.g. related to who maintains it, security etc.
- potential interest for compute - containerised
 - ESGF2 is likely to deploy from Kubernetes
 
DH: Note that GeoServer is written in Java - that might be a problem for a primarily Python community.

AS: We have used GeoServer in the past for various projects. It is a very useful tool in the GIS world, and we have found it useful for WMS and WFS. It can interface to many backends (such as PostgreSQL/PostGIS) and it can integrate with some basic profiles of NetCDF but we might not support our ESGF approach.

SA: There is a separate approach for using RPC to run code remotely.
- E.g. `func(x)` could be run remotely
- Key issue: security - how would it work?
- Would allow the user to run Python locally and run it on the remote server.

DH: Generally, from our platform - people mostly use the programming environment in Jupyter. But people don't have that option in ESGF nodes - because of the scale. We need to keep a simple (python) client that can do remote processing.

DH: Ouranos are working on a way to represent a unified interface to multiple remote services - so that the users can find multiple services in a single interface.

DH: **Dask** plays badly with Python WPS (**PyWPS**) - using the default job process launcher. If you switch to Async processes then it overcomes it. 

AS: For ESGF in general, I think we will need both Async and Sync responses - to deal with large jobs.

RJ: A lot people here like using Jupyter Notebooks. There are Jupyter servers at ANL and other sites. You need accounts to get access.

CE: Regarding ESGF Security, we have a security layer in front of the WPS. It can talk to Keycloak - currently it only checks if the user has an account or not. We would probably put a security filter in front of the WPS service endpoint.

SA: At the very least, we will need registration of users.

AS: Maybe we need to manage resources better, including using API Keys to track usage - and maybe limit access.

DH: It would entirely acceptable to use API Keys.

DH: It would be good to look at caching mechanisms in order to save resources. E.g. specifically for teaching example requests.

AS: We have been looking in detail at the use of **Kerchunk**, because it has the potential to allow us to expose all our data on disk through an S3 (object-store) interface. This would remove the need for duplication and could open up the door for all ESGF Data Nodes to allow access to applications across the internet (e.g. the PANGEO stack).

SA: Kerchunk could be good for subsetting, but wouldn't necessarily work for averaging and other functions.

DH: 
- We studies **Kerchunk** last year, and found out:
 - some metadata was lost (in axes)
 - some NaN could corrupt the arrays
 - for small files: storage for Kerchunk could be larger than NetCDF files
 - could only concatenate/merge files along a single dimension
- Things will need to be fixed to make it ready for production

SA: There is definitely a trade-off.

DH: **xncml** (version 1) - allows you to open an Xarray Dataset from NcML. It could play well with Kerchunk. This should work fine with a remote NcML file (e.g. via a Thredds server).

RJ: Has anyone thought of offering users a menu of options?

AS: Our "roocs" framework, proposed as the foundation for the ESGF Compute Node, allows the user to interrogate:
- which operations are available
- which arguments are available for each operation
    This could be exposed in a more user-friendly way.

### Next meeting:

- Date: 09/01/2023
 
