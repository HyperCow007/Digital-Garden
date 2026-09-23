---
{"dg-publish":true,"permalink":"/map/map-vaeloris-untitled-1/","created":"2026-09-23T15:33:09.119+09:30","updated":"2026-09-23T15:33:24.019+09:30","dg-note-properties":{"map_height_y":2388,"map_width_x":1668,"scale_pixels":10000,"scale_pixels_range":100000,"mapCalc1":10,"Updated":null}}
---


> [!NOTE]- Quick Calculator  
> Map Height in Pixels: `INPUT[number:map_height_y]`  
> Map Width in Pixels: `INPUT[number:map_width_x]`  
> lat: `VIEW[{map_height_y} / 2][math]`  
> long: `VIEW[{map_width_x} / 2][math]`  
> How Many Pixels In Scale: `INPUT[number:scale_pixels]`  
> How Many Units in Scale: `INPUT[number:scale_pixels_range]`  
> Scale: `VIEW[1/({scale_pixels}/{scale_pixels_range})][math:mapCalc1]`

[Pasted image 20260923150524.png](/img/user/Images/Pasted%20image%2020260923150524.png)

```leaflet  
id: VaelorisMap ### Must be unique with no spaces  
image: [Pasted image 20260923150524.png](/img/user/Images/Pasted%20image%2020260923150524.png) ### Link to the map image file. Do not add a ! in front of the image  
bounds: [[0,0], [2388, 1668]] ### Size of the map in px Height_y, Width_x. Ignore 0,0  
height: 850px ### Size of the leaflet embed in px on your screen  
width: 95% ### Size of the leaflet embed in your note  
lat: 1194 ### To center the map, make this half of the map height.  
long: 834 ### To center the map, make this half of the map width.  
minZoom: -1.5 ### Controls how far away from the map you can zoom out. Hover over the target icon to see the current level.  
maxZoom: 1 ### Controls how far towards the map you can zoom in. Hover over the target icon to see the current level.  
defaultZoom: -1 ### Sets the default zoom level when the map loads. Hover over the target icon to see the current level.  
zoomDelta: 0.5 ### Adjust how much the zoom changes when you zoom in or out.  
unit: miles ### The value displayed when measuring so you know what type of unit is being measure.  
scale: 1.5 ### Real units/px (resolution) of your map  
recenter: false  
darkmode: false ### marker
```
