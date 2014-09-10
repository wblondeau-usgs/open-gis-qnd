# The OGC Web Map Service (WMS)

#### Proper name:

The OpenGIS® Web Map Service Interface Standard

#### Purpose/Reason for existing:

Provides a visual rendering of a map.


##Logical Model of WMS

The essential logic of the WMS is described by **layers** and **maps**.

### WMS Layers

A Layer is a particular _kind_ of geospatially indexed information. "Geospatially indexed" means that, for any specification of coordinates (and coordinate systems are a whole 'nother thing) _there must exist a specific value of the Layer's defined measurement._ 

Now, there are a couple of caveats here, about that term "specific value".

First, it's possible for layers to be _sparse_, meaning that no measurement is available that can be returned for a given point. So, "specific value" can be logically null.

Second, it's entirely possible that there have been multiple measurements of a layer's type over time. It is therefore possible that the "single value" is a time series at a particular location.

Any WMS service may or may not offer a given Layer: it can only supply what is available in its data store, after all. (Of course, the WMS service might not supply all of the layers that are available in its data store.)

**Examples of Layers:**
 - annual rainfall measurements
 - residence locations
 - altitude above sea level
 - land use zoning
 - surface water average pH
 - population density
 - soil type
 - density of Tex-Mex restaurants

All of these could be valid layers, and a WMS could provide any or all of them. The key criterion, however, is that the data must must be geospatially indexed.

### WMS Maps

A WMS Map is a pictorial rendering of requested Layer data for a requested geospatial area.

There. That didn't hurt too much, did it?

There are some details though.

"Requested geospatial area" means a specification of a _geometry_ using a _coordinate system_.

A coordinate system is a whole 'nother story. Latitude/longitude/altitude are the most ordinary one encountered; altitude may be irrelevant or absent.

A Geometry is a geometrically defined shape (in other words, one on which you can use math to include/exclude any coordinate reference.) The most common geometries are:
 - **point**
 - **point with radius (aka "circle")**
 - **bounding box:** This one is a 4-sided geometry, of which the sides are isometric to the coordinate system. In other words, a lat/long bounding box would be defined by a north latitude, a south latitude, an east longitude, and a west longitude. Note that, due to the grim meathook realities of spherical geometry, there is nowhere on the earth's surface where the bounding box forms the mathematically exact planar rectanglethat the word "box" would lead you to expect. (Smallish boxes close to the equator make a pretty close approximation, of course.)
 - **polygon:** a sequence of geospatial coordinate points that, when followed, forms a closed shape. Why would someone do something so exotic? Well, most often, to define a geometry that has a real-world significance, such as the country of Switzerland, the Kickapoo River drainage basin, or the geographical regions in which the Haussa language is spoken by more than 15% of the population.


## Operations

###

#### Request parameters:




