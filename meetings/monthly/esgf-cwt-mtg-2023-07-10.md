# ESGF Compute Working Team Meeting - 2023-07-10

## Logistics

Where: https://whereby.com/cafe-pingu

When:  10/07/2023

Who:  ESGF CWT:
- Carsten Ehbrecht (DKRZ)
- Christian Pagé (CERFACS)
- Alessandra Nuzzo (CMCC)
- Ezequiel Cimadevilla (Uni Can)
- Marco Mancini (CMCC)
- Sasha Ames (LLNL)
- Paola Nassisi (CMCC)
- Valentina Scardigno (CMCC)
- Zach Price (ORNL)

Missing:
- Ag Stephens (STFC CEDA)
- David Huard (Ouranos)

## Actions

- [ ] ASte/CE Consider Jenkins and other CI systems for potentially running the test suite - **ongoing**
- [ ] ASte: look at parquet as Kerchunk format - does it help us with large file problems - **ongoing**
- [ ] ASte/CE: think about `roocs` caching of remote data - **Ongoing - meeting on Friday**
- [ ] ASte/CE: Update the diagram to cope with the case of multiple inputs from multiple nodes - might need the multi-step at the start of the diagram - **ongoing**
- [ ] ASte/CE: Implement the API KEY/proxy from the start. We might be able to use Keycloak to provide this. - **Ongoing - meeting on Friday**
- [ ] DH: Keep CWT informed of developments regarding WMO + ESGF interactions - **Ongoing**

## Agenda

The Agenda for today is:
 
* Presentation 1: The CMCC Data Delivery System: Marco Mancini (CMCC)
* Presentation 2: The ESGF Virtual Aggregation: Ezequiel Cimadevilla (Uni of Cantabria)
* Discussion
  
## Notes

1. Presentation CMCC Data Delivery System

* CDS ui
* 35 datasets (150 TB)
* 160 000 requests
* kubernetes
* datastore: intake
* cache for acceleration
* next version: use mongodb for metadata access
* query engine: rabit mq ... dask geokube
* auth: keycloak
* DDS rest api
    * datasets: get medata, query, estimate
    * request: status, size, url
* clients: ogc, web portal, python client, rest api
* json request similar to CDS
* workflow: use networkx ... simple json description
* dds python client ... similar to CDS
* use geokube to open dataset
* forked rook wps: replaced internal codes by DDS api calls
    * need api_key

geokube:
* developed by cmcc
* extesnion of xarray
* unit-aware geo referenced
* regrid with xesmf
* use plotly

qa:
* Q: christian

My question is do you plan to plug-in more advanced calculations like climate indices (icclim) which requires also large input  data and result in large data reduction because it output annual or seasonal data, or you plan to stay with only the basic operators you have now

* A: marco: yes

2. Presntation ESGF Virtual Aggregation

* java ncml ... virtual aggreagtions
* opendap
* experiment with cmip6
* ncml + opendap + thredds tds
* performance test of opendap ... 100 MB/s ... similar as retrieving cmip6 form google cloud
* issues with large ncml file
* issue with ipcc atlas cmip6 ... chunk size 1 for time for some datasets
* adding fixes into ncml
* opendap vs kerchunk: 
    * opendap sends chunks uncompressed
    * kerchunk + zarr ... compressed


