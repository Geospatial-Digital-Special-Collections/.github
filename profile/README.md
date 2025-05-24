## Geospatial Digital Special Collections

# GDSC - Geospatial Data Special Collections

GDSC is a set of configurations and tools to curate special collections of GIS data.  

Currently it includes a back end data store in a containerized k8s environment, a set of tools for data management and curation, and a front end search engine to browse the data catalog.

### Installation

Please see the [installation notes](https://github.com/Geospatial-Digital-Special-Collections/docs/blob/main/md/gdsc_install.md) in the [docs](https://github.com/Geospatial-Digital-Special-Collections/docs) repository.

### Components

There main repositories for GDSC are:  
1. [kubernetes](https://github.com/Geospatial-Digital-Special-Collections/kubernetes)  - tools for managing the k8s cluster  
2. [tools](https://github.com/Geospatial-Digital-Special-Collections/tools) - to manage data curation and ingest  

There are several other key components to GDSC:
1. [metadata repository](https://miami.box.com/s/cpe136whxprafac9ssvkig74ju4o2x7m) - currently an excel file stored on Box
2. [docker](https://github.com/Geospatial-Digital-Special-Collections/docker) repository used to build containers used by GDSC

Note: the kubernetes repository can also be run on localhost as a development machine and managed by the tools repository on the same development machine.  

### Services and Endpoints

The above components provide several internet services (development machine):
1. A simple search interface at https://gdsc.idsc.miami.edu (http://localhost:5000)
2. A vector tile server at https://gdsc.idsc.miami.edu/vector/ (http://localhost:7800)
3. A SOLR index of the metadata repository at https://gdsc.idsc.miami.edu/solr/solr/ (http://localhost:8983)
4. A PostgREST endpoint for database queries at https://gdsc.idsc.miami.edu/functions/ (http://localhost:3000)

The GDSC data store is also linked to an ArcGIS Portal server at https://portal.gdsc.miami.edu (not part of the Kubernetes implementation).

### Documentation

For most documentation see the README files in respective directories of each repository in this organization. A few general notes are in the [docs](https://github.com/Geospatial-Digital-Special-Collections/docs) repository for:

-   [general architecture](https://github.com/Geospatial-Digital-Special-Collections/docs/blob/main/figures/gdsc_implementation_v2.svg)
-   [one page summary description](https://github.com/Geospatial-Digital-Special-Collections/docs/blob/main/md/gdsc_summary.md)
-   [installation notes](https://github.com/Geospatial-Digital-Special-Collections/docs/blob/main/md/gdsc_install.md)

### Questions

Please direct all questions to [tnorris@miami.edu](mailto:tnorris@miami.edu)
