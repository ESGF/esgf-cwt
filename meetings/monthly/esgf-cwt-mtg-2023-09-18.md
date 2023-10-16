# ESGF Compute Working Team Meeting - 2023-09-18

## Logistics

Where: Zoom

When:  18/09/2023

Who:  ESGF CWT:
- Ag Stephens (STFC CEDA)
- Carsten Ehbrecht (DKRZ)
- Sasha Ames (LLNL)
- David Huard (Ouranos)
- Ezequiel Cimadevilla (Uni Can)
- Alessandro Spinuso (KNMI)
- Alessandra Nuzzo (CMCC)
- Maxwell Grover (ANL)
- Charles Gauthier (Ouranos)
- Neil Massey (STFC CEDA)
- Paola Nassisi (CMCC)
- Ben Coalson (ORNL)
- Prashanth Dwarakanath Roa (LIU)
- Forrest Hoffman (ORNL)

## Actions

- [ ] ASte/CE Consider Jenkins and other CI systems for potentially running the test suite - **ongoing**
- [ ] ASte/CE: think about `roocs` caching of remote data - **Ongoing - meeting on Friday**
- [ ] ASte/CE: Update the diagram to cope with the case of multiple inputs from multiple nodes - might need the multi-step at the start of the diagram - **ongoing**
- [ ] ASte/CE: Implement the API KEY/proxy from the start. We might be able to use Keycloak to provide this. - **Ongoing - meeting on Friday**
- [ ] DH: Keep CWT informed of developments regarding WMO + ESGF interactions - **Ongoing**
- [ ] AS/CE: look at CMOR Fixer (https://github.com/EC-Earth/cmor-fixer) - which appends a line to headers noting that it has been processed

## Agenda

### 1. Welcome and introductions

### 2. Actions and minutes from last meeting

Last meeting (2023-07-10) was a discussion meeting:
* Presentation 1: The CMCC Data Delivery System: Marco Mancini (CMCC)
* Presentation 2: The ESGF Virtual Aggregation: Ezequiel Cimadevilla (Uni of Cantabria)
* Discussion

- [ ] ASte/CE Consider Jenkins and other CI systems for potentially running the test suite - **ongoing**
- [x] ASte: look at Parquet as Kerchunk format - does it help us with large file problems - **done**:
  * Parquet looks useful because it enables _lazy loading_ of metadata.

- [ ] ASte/CE: think about `roocs` caching of remote data - **Ongoing - meeting on Friday**
- [ ] ASte/CE: Update the diagram to cope with the case of multiple inputs from multiple nodes - might need the multi-step at the start of the diagram - **ongoing**
- [ ] ASte/CE: Implement the API KEY/proxy from the start. We might be able to use Keycloak to provide this. - **Ongoing - meeting on Friday**
- [ ] DH: Keep CWT informed of developments regarding WMO + ESGF interactions - **Ongoing**

### 3. Discussion

#### Merging `roocs-utils` content into `clisops` withing roocs

Overview: https://roocs.github.io/overview/

NOTE: current imports are:

```
from roocs_utils import foo
```

IF WE CHANGE THE NAMESPACE: we would need to change them to:

```
from clisops.roocs_utils import foo
```

STEP 1: backward-compatible migration of `roocs_utils` library:
- move `roocs-utils::roocs_utils` into `clisops::`
- move `roocs-utils::tests/*` into `clisops::tests/test_roocs_utils/`
- change `clisops::setup.py` to include `roocs_utils` in `find_packages(...)` etc
- NOTHING WILL BREAK
- Deprecate/close the library. Update docs to say it has been moved.

STEP 2: migrate code components from `roocs_utils` into parts of `clisops` library:
- THINGS MIGHT BREAK
- Move modules and packages from `roocs_utils` into appropriate parts of `clisops`
- Move unit tests from `tests/test_roocs_utils` into parts of `tests/`
- Update `rook`, `daops`, `dachar` and `clisops` so that imports (and tests) all work
- Release new versions of all packages

#### Experiments with Kerchunk, Parquet etc

- Parquet is a column-oriented tabular data format:
  - it can be used to store Kerchunk content
  - it splits content into multiple files so enables _lazy-loading_ of metadata
- Kerchunk with HTTP(S) instead of S3:
  - at CEDA, we are working on building Kerchunk on top of the HTTPS endpoints already provided by our data nodes.
- xarray `xpublish` vs `Kerchunk`
  - EC has done some work to compare these
  - Generation of Kerchunk files is a costly process

- [ ] AS/CE: discuss in more detail with EC

#### Ag change of role, implications/opportunities

- CEDA: Alan Iwi, Neil Massey being more involved
- CWT Co-chair: open

#### Improving the test coverage (of data) for roocs

Currently reviewing a Pull Request to add in automated testing:

https://github.com/roocs/daops/blob/test_data_pools_new/tests/data_pools_checks/run_data_pools_checks.py#L793

Additional actions:
 - [ ] clisops/xarray versions in the ResultsDB? - needs to be in there
 - CSV file - how to merge parallel results from different sites
	  - needs a merge capability

#### Ability for `daops` to read Kerchunk files:

See: https://github.com/roocs/roocs-utils/issues/106

#### Ouranos work on CWT

- DH:
  - CG, working at Ouranos, will be to embed polygon averaging into "roocs"
    - to allow sending in a Shapefile to define the polygon and then returning the subset within it

#### Interactions with the WMO regarding WIS:
- DH: We had a meeting with Tom Kralidis, to discuss WMO WIS system. Uses a federated system around the globe - like ESGF.

#### CMOR-Fixer

PDR:
- Take a look at CMOR Fixer - developed by KNMI - lots of fixing
- [ ] AS/SA to look at CMOR Fixer
  - https://github.com/EC-Earth/cmor-fixer
  - it appends a line to headers noting that it has been processed

### 4. Next steps:


### 5. AOB:

Next meeting: 16th October 2023



