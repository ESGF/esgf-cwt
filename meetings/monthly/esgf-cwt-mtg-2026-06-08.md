# ESGF Compute Working Team Meeting - 2026-06-08


## Logistics

Where:

https://whereby.com/tea-room-cwt

When:  08/06/2026

* 16:00 - 17:00 Hamburg
* 15:00 - 16:00 UTC
* 10:00 - 11:00 Montreal
* 07:00 - 08:00 San Francisco

Who:

- Carsten Ehbrecht (DKRZ)
- (all on vacation)

not attending:
- David Huard (Ouranos)
- Nils (ECMWF)
- Alessandro (KNMI)
- Sasha (LLNL)
- Zach Price (ORNL)
- Forrest Hoffman (ORNL)


## Agenda

### 1. Welcome and introductions

### 2. Actions and minutes from last meeting

- [ ] Carsten + David: work on pygeoapi + STAC
- [ ] Carsten: work on docker deployment
- [ ] Carsten etc: Write JOSS paper about Rook+clisops
- [ ] Carsten etc: WPS integration into STAC
- [ ] Carsten + David: add something for the compute service ... as PR (Sasha). Add David as reviewer.
    - https://github.com/WCRP-CMIP/cmip7-guidance/blob/docs/docs/CMIP7/Guidance_for_ESGF.md

### 3. Presentation (optional)

See list of presentations in issue https://github.com/ESGF/esgf-cwt/issues/35.

### 4. Discussion

#### Round Table

Alessandro:
* DONE: i like to have the recordings of the cds GA
* https://climate.copernicus.eu/9th-c3s-general-assembly

Nils:
```
Here are the recordings: 
https://climate.copernicus.eu/9th-c3s-general-assembly

It was a really nice GA with many highlights. 

I recommend the opening session 

Péter Kajner (WWF) The Role of Climate Services in Addressing the Challenges of Climate Change for Hungary. 
Peter will possibly be new secretary of state in the new government. 

Suraje Dessai (ESABCC) Strengthening resilience to climate change in Europe  and the role of climate services


Day 2 
Samantha Burgess (ECMWF) Climate Intelligence update

Session 11:00 - 12:30 

And the entire Friday both sessions. The roundtable discussion about the future of Climate services is very interesting and I am glad that we have the statements now as a reference. 


Next GA is end of May 2027 in Rome. Save the date in your calendar :-) 
```

Carsten:
* woodpecker demo continued:
    * https://github.com/cehbrecht/woodpecker
    * Demo for fixing library ... inspired by Ruff Python linter
    * refinement about vocabulary and usage
* started new test data repo:
    * https://github.com/cehbrecht/mini-climate-data
    * using recipes to build reduced test data from original data

### 5. Next steps:

* Work on pygeopi and STAC. 
* Need a new cookiecutter and birdy. 
* Work on docker deployment. 
* Integrate with S3 storage!!!
* Need a production ready (better queue) pygeoapi.
* Work on prov db for Rook WPS
* Write JOSS paper about Rook+clisops. See xclim example: https://joss.theoj.org/papers/10.21105/joss.05415
* WPS integration into STAC: https://github.com/ESGF/esgf-roadmap/issues/134

### 6. AOB:

Next meeting: 13th July 2026

