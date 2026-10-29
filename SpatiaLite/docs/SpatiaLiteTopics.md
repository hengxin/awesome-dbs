# SpatiaLite Topics

- 来源: https://www.gaia-gis.it/gaia-sins/spatialite_topics.html
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

# SpatiaLite Topics
# Quick reference list to Wiki pages
last updated: 2018-08-20
Back to the [SpatiaLite](https://www.gaia-gis.it/fossil/libspatialite/home) home page
- [Virtual Interfaces](#topic_virtual_interfaces)
- [Summaries of topics on major version changes](#topic_version_changes)
- [Spatialite Topology (5.0.0)](#topic_topology)
- [Spatialite Tools](#topic_tools)
- [Spatialite CookBook (5.0.0)](http://www.gaia-gis.it/gaia-sins/spatialite-cookbook-5/index.html)
- [SQL functions reference list (latest relesed version)](http://www.gaia-gis.it/gaia-sins/spatialite-sql-latest.html)
- Short topics (referenced from other pages)
- [5.0.0: Drop-RenameTable and RenameColumn](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=Drop-RenameTable+and+RenameColumn)
- [5.0.0: ImportSHP(), ExportSHP(), ImportDBF() and ExportDBF()](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.4.0+functions#1)
- [5.0.0: SQL functions manipulating Sequences](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.4.0+functions#2)
- [5.0.0: The ST_Cutter() SQL function](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=ST_Cutter)
- [5.0.0: The GetShapefileExtent SQL function](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=about+GetShapefileExtent%28%29)
- [5.0.0: Importing GPX Tracks](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=GPX+tracks)
- [5.0.0: Searching Nearest Neighbors: VirtualKNN](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=KNN)
- [5.0.0: ISO SQL/MM Topology](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=ISO+Topology)
- [5.0.0: SQL Functions and DE-9IM Intersection Matrices](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=about+DE-9IM)
- [5.0.0: About the BLOB-TinyPoint internal encoding](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=BLOB-TinyPoint)
- [5.0.0: SQL Procedures, Stored Procedures and Stored Variables: a quick intro](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=Stored+Procedures)
- [4.3.0: Persistent Connection Modifiers](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.3.0+functions#2)
- [4.3.0: Trigonometry](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.3.0+functions#3)
- [4.3.0: Pathname manipulation](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.3.0+functions#4)
- [4.3.0: URL manipulation](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.3.0+functions#5)
- [4.3.0: Affine Transformations support](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=Affine+Transform)
- [4.3.0: Ground Control Points support](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=Ground+Control+Points)
- [4.3.0: SE Styling helpers](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.3.0+functions#8)
- [4.3.0: Extended SRID Inspection](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=SRID+Inspection)
- [4.3.0: Comprehensive list of all dot macros available in the SQL scripting environment](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=dot+macros)
- [4.2.1: Using CloneTable()](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=CloneTable)
- [4.2.0: DMS / DD conversions](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.2.0+functions#2)
- [4.2.0: Geometry processing](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.2.0+functions#3)
- [4.2.0: Forcing Layer Statistics to be recalculated](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.2.0+functions#4)
- [4.2.0: ROWID checks](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.2.0+functions#5)
- [4.2.0: building/updating a MetaCatalog](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.2.0+functions#6)
- [4.2.0: GEOS / LWGEOM errors and warnings](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.2.0+functions#7)
- [4.2.0: GPKG (GeoPackage) support](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.2.0+functions#8)
- [4.2.0:How-to handle a MetaCatalog (practical example)](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=metacatalog)
- [4.2.0:How-to fully identify Invalid Geometries (practical example)](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=invalid-geometries)
- [4.1.0: Speed enhancements introduced in 4.1.0](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=speed-optimization)
- [4.1.0: New XML-related functions (ISO 19115 Metadata, SLD/SE styles, SVG graphics)](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=XmlBlob+and+VirtualXPath)
- [4.1.0: New WFS embedded client (directly feeding a DB from a WFS datasource)](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=WFS)
- [4.1.0: New DXF internal support (directly importing and exporting CAD drawing files)](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=DXF)
- [4.1.0: The binary format specification supporting XmlBlob](https://www.gaia-gis.it/gaia-sins/xmlBlob/XMLBlob.html)
- [4.1.0: SQL functions supporting data-type casting](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.1.0+Changes#cast)
- [4.1.0: SQL functions supporting circles, ellipses, arcs and sectors](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=circles-ellipses)
- [4.1.0: Spatial Index: best practices](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=SpatialIndex)
- [4.1.0: Shadowed ROWID issues](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=Shadowed+ROWID+issues)
- [4.1.0: Unsafe SQL functions conditionally depending on SPATIALITE_SECURITY=relaxed](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.1.0+Changes#unsafe)
- [4.1.0: Importing and exporting geospatial data as CAD drawing files](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=DXF)
- [4.1.0: GPX tracks: a quick intro](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=GPX+tracks)
- [4.1.0: SQL functions for Global Area Reference System (GARS)](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=GARS)
- [4.1.0: SLD/SE Styling - Introduction](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=SLD/SE+Styling)
- [4.1.0: XmlBlob and VirtualXPath](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=XmlBlob+and+VirtualXPath)
- [4.1.0: XmlBlob - Quick start](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=XmlBlob-intro)
- [4.1.0: Metadata references - a practical example](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=Metadata+references)
- [SQLite 3.7.17 experimental extensions](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=sqlite-3.7.17-extra)
- [4.0.0: Using the spatialite_convert tool](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=switching-to-4.0#convert)
- [4.0.0: Supporting Writable Views](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=writable-view)
- [4.0.0: Dynamically loading mod_spatialite as an extension module](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=mod_spatialite)
- [4.0.0: SQL functions supporting Tesselations (regular grids, Delaunay triangulations, Voronoj diagrams and ConcaveHull)](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=tesselations-4.0)
- [4.0.0: Relevant changes introduced in version 4.0.0](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=switching-to-4.0)
- [4.0.0: SQL Statements Log as implemented in version 4.0.0](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=SQL+Log)
- [4.0.0: Tessellation-related SQL functions supported in version 4.0.0](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=tesselations-4.0)
- [4.0.0: Changes in GUI and CLI tools supporting version 4.0.0](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=tools-4.0)
### Virtual Interfaces
What is a Virtual Interface
SQLite has the nice capability to support [Virtual Tables](https://www.sqlite.org/vtab.html), that is a powerfull mechanism allowing to greatly extend the basic capabilities of the SQL language.
A Virtual Table is not really a table (it actually is a piece of executable code), but designed in such a way that it supports all the usual SQL operations: CREATE TABLE , DROP TABLE , SELECT , and is some cases INSERT , UPDATE and DELETE (Virtual Tables usually can only support READ-ONLY operations; supporting unrestricted READ-WRITE operations is rather exceptional).
Virtual Tables can be seen as Interfaces , because they are intended to support typical SQL operations on something external to the ordinary Database logic.
There are two big families of Virtual Interfaces:
- Virtual Interfaces allowing to directly access data stored outside the Database, or stored within the Database but adopting some non-native encoding.
- Virtual Interfaces accessing external datasources: VirtualShape , VirtualDBF , VirtualText , VirtualXL , VirtualPostgres
- Virtual Interfaces converting to/from non-native Geometries: VirtualFDO , VirtualGPKG
- Virtual Interfaces allowing to query the results of some more or less complex Algorithm.
- VirtualRouting , VirtualKNN and so on
## Virtual Interface Topics
Topic Wiki page Initial introduction
Direct access to external ShapeFiles: VirtualShape [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=Virtual+Tables+(misc)#VirtualShape) since version 1.0
Direct access to external DBF Files: VirtualDBF [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=Virtual+Tables+(misc)#VirtualDBF) since version 2.4.0
Direct access to external Text Files ( *.txt , *.csv) : VirtualText [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=Virtual+Tables+(misc)#VirtualText) since version 2.2.0
Direct access to external MS Excel spreasheets ( *.xls ): VirtualXL [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=Virtual+Tables+(misc)#VirtualXL) since version 2.4.0
Direct access to external PostgreSQL/PostGIS DBMS: VirtualPostgres [read](https://www.gaia-gis.it/fossil/virtualpg/wiki?name=tutorial) N.A. independent package ( 2011 )
Automatic conversion to/from FDO Geometries: VirtualFDO [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=Virtual+Tables+(misc)#VirtualFDO) since version 2.3.0
Automatic conversion to/from GeoPackage Geometries: VirtualGPKG [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=Virtual+Tables+(misc)#VirtualGPKG) since version 4.0.0
Sql based Routing module: VirtualRouting [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=VirtualNetwork+reloaded) since version 4.5.0
Searching Nearest Neighbors: VirtualKNN [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=KNN) since version 4.4.0
Separate complex geometries into distinct elements: VirtualElementary [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=VirtualElementary) since version 4.2.1
Module that enables SpatiaLite to directly perform XPath queries : VirtualXPath [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=VirtualXPath-intro) since version 4.1.0
Access different datasources using Gdal/Ogr: VirtualOGR [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=VirtualOGR) N.A. independent package ( 2012 )
Obsolete former Routing module: VirtualNetwork used with spatialite_network , replaced with VirtualRouting [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=VirtualNetwork+reloaded) since version 4.2.1
### Spatialite Tools
The Spatialite Tools Fossil Repository
- is contained in a seperate repository (all links will not return to this page)
The [main SpatiaLite-Tools Wiki page](https://www.gaia-gis.it/fossil/spatialite-tools/index)
## List of Spatialite Tools Topics
Topic Wiki page Initial introduction
a complete CLI front-end, more or less equivalent to the well known sqlite3 front-end, but fully supporting SpatiaLite: spatialite [read](https://www.gaia-gis.it/fossil/spatialite-tools/wiki?name=version+4.2.0) since version 4.4.0
Create, Update, Query a Dem-Database: spatialite_dem [read](https://www.gaia-gis.it/fossil/spatialite-tools/wiki?name=spatialite_dem) since version 4.5.0
spatialite_osm_map/raw/filter/filter and overpass : OSM tools [read](https://www.gaia-gis.it/fossil/spatialite-tools/wiki?name=version+4.2.0) since version 4.4.0
Using the spatialite_convert tool [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=switching-to-4.0#convert) since version 4.0.0
### Spatialite Topology (5.0.0)
Under development
## ISO Topology: Index
Topic Wiki page Initial introduction
ISO Topology: a quick intro: Spatialite Topology - 01 [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=topo-intro) since version 5.0.0
Topology: basic DB layout: Spatialite Topology - 02 [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=topo-layout) since version 5.0.0
Topology-Geometry: ISO SQL Functions: Spatialite Topology - 03 [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=topo-iso-sql) since version 5.0.0
Topology-Network: ISO SQL Functions: Spatialite Topology - 04 [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=toponet-iso-sql) since version 5.0.0
Topology editing by using basic ISO SQL function: Spatialite Topology - 05 [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=topo-start) since version 5.0.0
Network editing by using basic ISO SQL function: Spatialite Topology - 06 [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=toponet-start) since version 5.0.0
Topology-Geometry: an intermediate tutorial: Spatialite Topology - 07 [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=topo-intermediate) since version 5.0.0
Topology-Geometry: an advanced tutorial: Spatialite Topology - 08 [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=topo-advanced) since version 5.0.0
### Summaries of topics on major version changes
Relevant changes for major versions
## Relevant changes for major versions
Topic Wiki page Initial introduction
Documentation and Tutorials about recent changes and new features: 4.3.0 [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.2.0-doc) since version 4.3.0
Documentation and Tutorials about recent changes and new features: 4.2.0 [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.2.0-doc) since version 4.2.0
New SQL functions introduced in: 4.2.0 [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.2.0+functions) since version 4.2.0
New SQL functions introduced in: 4.1.0 [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.1.0+Changes) since version 4.1.0
Documentation and Tutorials: 4.1.0 [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=4.1.0-doc) since version 4.1.0
Switching to: 4.0.0 [read](https://www.gaia-gis.it/fossil/libspatialite/wiki?name=switching-to-4.0) since version 4.0.0
last updated: 2018-08-20
Back to the [SpatiaLite](https://www.gaia-gis.it/fossil/libspatialite/home) home page