## Geospatial Digital Special Collections

# GDSC - Geospatial Data Special Collections

This organization contains an initial set of tools to curate special collections of GIS data as services through standard open and selected proprietary protocols. Currently it includes a back end data store in a containerized kubernetes environment, a set of tools for data management and curation, and a front end search engine to browse the data catalog.

There are several key components to GDSC:
1. metadata repository: currently an [excel file](https://miami.box.com/s/cpe136whxprafac9ssvkig74ju4o2x7m) stored on Box
2. kubernetes cluster with rook-ceph storage and a clone of the [https://github.com/Geospatial-Digital-Special-Collections/kubernetes](kubernetes) repository (current control plane at kmaster.idsc.miami.edu)
3. administrative machine with a clone of the [https://github.com/Geospatial-Digital-Special-Collections/tools](tools) repository (your data management and curation machine)
4. a set of custom container images in the [https://github.com/Geospatial-Digital-Special-Collections/docker](docker) repository used by the kubernetes implementation

Note: the kubernetes repository can also be run on localhost as a development machine and managed by the tools repository on the same development machine.  

These components provide several internet services (development machine):
1. A simple search interface at https://gdsc.idsc.miami.edu (http://localhost:5000)
2. A vector tile server at https://gdsc.idsc.miami.edu/vector/ (http://localhost:7800)
3. A SOLR index of the metadata repository at http://10.141.251.20:8983 (http://localhost:8983)
4. A PostgREST endpoint for database queries at http://10.141.251.21:3000 (http://localhost:3000)

The GDSC data store is also linked to an ArcGIS Portal server at https://portal.gdsc.miami.edu (not part of the Kubernetes implementation).

### Documentation

For most documentation see the README files in respective directories of each repository. A few general notes are in the [https://github.com/Geospatial-Digital-Special-Collections/docs](docs) repository for:

-   [general architecture](docs/gdsc_implementation.svg)
-   [one page summary description](docs/gdsc_summary.md)

### Questions

Please direct all questions to [mailto:tnorris@miami.edu](tnorris@miami.edu)
