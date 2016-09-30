---
layout: post
title: Crawling Satellite Imagery from Bing Maps
categories: remote-sensing satellite-imagery Bing
---

People can find a lot of free sources of satellite imagery such as Sentinel-1, Sentinel-2 of the Copernicus program
and Landsat-8 of NASA. However a cloud-free and global basemap like that of Google or Bing is not trivial to obtain.
Before writing this post, I did not know that DigitalGlobe, partnering with Amazon, has released [SpaceNet]()with very high
resolution imagery from WorldView satellites. I wish I knew this earlier but anyway SpaceNet is limited and at the time 
I write this, just the imagery of Rio De Janeiro was released.

The good thing is both APIs of Google Maps and Bing Maps allow users to download a limited amount of "patches" each month.
To me this is more than enough. The rest is to stitch patches together into a large map. 

Steps to download a satellite image of a geographical place is as follows:
1. Given a location, e.g Manchester
2. Using reverse geocoding service to get the longitude and latitute of the location
3. Determine the extent of the area, either manually or automatically wrt the given bounding box. Most of the time that 
bounding box is much larger than the area. So you may want to limit the maximum image size.
4. Given a [zoom level](), calculate a meshgrid of points whose coordinates (lat,lon) will be used to call the API. At this step,
the longitude and latitude in degrees are converted into pixel coordinates. 
5. Once all patches are retrieved, stitching them together.

Reverse geocoding is also provided by Google and Bing. I choose [Nominatim](), a geocoding service based on [OpenStreetMaps]()
with no particular reason for steps 1-2-3. Step 4 is quite complicated for guys have no knowledge of how Earth is indexed.
The best explanation comes with the picture below
![hehe](http://www.learner.org/jnorth/images/graphics/mclass/Lat_Long.gif) 

This article [Bing Map Tile System](https://msdn.microsoft.com/en-us/library/bb259689.aspx) from Bing explain how the Bing Map 
is shattered into tiles at every zoom level (there are 19 levels in total). There is a slight different between Bing and Google, 
in terms of coordinates as well as the basic batch size. Find out yourself.

Noticeably, each patch downloaded from Bing and Google is watermarked of course. I find Bing watermarking is more 'friendly'.
My repo scripts for this stuff is accessible at [gmapcrawler](https://github.com/vodp/mapcrawler), where a part of the 
code is borrowed from this [gmap_tiles](https://github.com/nst/gmap_tiles). More about geocoding tools can be found 
at [geopy](https://github.com/geopy/geopy). Happy responsible crawling!

