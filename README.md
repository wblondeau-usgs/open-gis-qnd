The Quick and Dirty Guide to OpenGIS Services
============

The Quick And Dirty guide to various open GIS specifications

_"It can be quick; it can be dirty; but true documentary synergy requires both."_

This repo is by intention a simple introduction to selected core specifications from the [Open Geospatial Consortium](http://www.opengeospatial.org/), together with some supporting specs. 

The reason for this guide is that most of the specifications in this space are reasonably well written as engineering documents, but are generally poor as high-level orientation resources. Note that this is not intended as a criticism of the OGC or any other specification author; it's a general problem. See the [World Wide Web Consortium](http://w3.org)'s specifications for a fairly famous example. The W3C has spawned a rich ecosystem of explanatory materials. Nothing like that is readily available for the open GIS standards. This guide is intended as a minor stopgap answer for that situation.

This guide is **not** intended to be a complete survey of the OGC specs; or in fact a complete survey of anything. It is ad-hoc. It may not be a sufficient resource for any given project. Not too many guarantees here.

What _is_ guaranteed is that:

 - Any spec addressed here will be clearly and simply described.
 - Any spec addressed here will include a link to official published specification
 - Any spec addressed here will include links to helpful non-normative resources
 - This guide will include notable incidents, peculiarities, gotchas, and easily missed points.

There are certain deliberate, systematic omissions in this guide:

 - Where important operations are specified in both [SOAP](http://en.wikipedia.org/wiki/SOAP) and URL-parameter request form, the SOAP form will be ignored. That's because this guide considers SOAP to be both obsolete and regrettable.

 - This guide will prioritize read/query operations over operations that are expected to cause state changes on the server. This is because this kind of initial orientation to the material is much more appropriate to (in RESTful terms) GET (and possibly HEAD) methods. Anyone wishing to perform transactional updates should really seriously study the normative specifications.

##The Services

 - **[Common Service Operations](services/common_operations.md):** Many Services share recurring operational components. Those are described here.
 - **[Web Map Service (WMS)](services/WMS.md):** Ask a question, get a map displaying the answers.
 
