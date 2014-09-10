## Common Operations

### GetCapabilities

A common metadata/discovery operation, mandatory for many OGC Services.

#### Parameters
Parameters are generic.
##### Mandatory:
 - REQUEST=GetCapabilities (fixed value identifying a GetCapabilities request)
 - SERVICE=(name of service for which GetCapabilities is being requested, e.g. WMS, WFS, etc)

##### Optional:
 - VERSION=(requested version)
 - FORMAT=(desired format of service metadata, expressed as [internet media type](http://en.wikipedia.org/wiki/Internet_media_type)) 
 - UPDATESEQUENCE=(sequence number or string for cache control)

#### Response
Response is specific to the individual service.
