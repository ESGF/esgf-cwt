# ESGF Compute Working Team Meeting - 2024-03-11


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  11/03/2024

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Maxwell Grover (ANL)
- Carsten Ehbrecht (DKRZ)
- Charles Gauthier (Ouranos)
- David Huard (Ouranos)
- Martin Schupfner (DKRZ)
- Ezequiel Cimadevilla (Uni Can)
- Forrest Hoffman (ORNL)
- Sasha Ames (LLNL)
- Zach Price (ORNL)

## Agenda

### 1. Welcome and introductions

### 2. Actions and minutes from last meeting

- [ ] Carsten: add wiki page for presenters
- [ ] Max test running rook on the US side - Ansible (ongoing)
- [ ] Neil follow up with CEDA group about STAC + elasticsearch process
- [ ] DH+Sasha+Max: Set up a mtg with Tom Kralidis to discuss WMO WIS - at ESGF F2F in April? or at least in CWT

### 3. Presentation (optional)

See list of presentations in issue https://github.com/ESGF/esgf-cwt/issues/35.

### 4. Discussion

Round Table:

Max:
* try get ansible playbooks running.
* working on rook branch:
    * https://github.com/mgrover1/rook
* using clisops in esgf-cookbook:
    * https://github.com/esgf2-us/esgf-cookbook
    * https://docs.google.com/document/d/18nVNFDOq7K8YKXb_-klrJsXewD7H6sDzIikh_E0Luwk/edit#heading=h.hrc5wii4n6kr 
* ESGF F2F registration is open:
https://bit.ly/48PQwhq

Charles:
* daops/clisops: PR with AverageShape operator is merged.

David:
* working with xpublish

Ezequiel:
* made a presentation at pangeo

Sasha:
* no updates ... looked at wps playbook
* ESGF F2F: maybe not the right scope for Tom Kralidis

Forrest:
* no updates

Zach:
* no updates

Martin:
* issue in xarray with cftime:
https://github.com/pydata/xarray/issues/7794
* this is blocking us from updating to a new xarray version (one year old) in clisops
* ... Sasha: maybe ask https://xarray.dev/team   ?
* ... David: I ask one of my collegues

Carsten: 
* updated ansible deployment for pywps with slurm. works on almalinux 9.x. still on dev branch:
https://github.com/bird-house/ansible-wps-playbook/tree/dev-almalinux9

Nils:
* OGC Innovation days in July 1-2, 2024, Tartu, Estonia
https://2024.europe.foss4g.org/schedule/ogc-euidays/ 


### 5. Next steps:



### 6. AOB:

Next meeting: 8th April 2024




 
 
 
 
 
