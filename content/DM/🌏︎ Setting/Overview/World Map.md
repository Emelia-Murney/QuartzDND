#World 

<center>An Interactive world map that has markers with links to their respective article.</center>
 
```leaflet  
id: WorldMap 
image: domeworld.png
bounds: [[0,0], [2748, 2748]] ### Size of the map in px Height_y, Width_x. Ignore 0,0  
height: 800px ### Size of the leaflet embed in px on your screen  
width: 100% ### Size of the leaflet embed in your note  
lat: 1374 ### To center the map, make this half of the map height.  
long: 1374 ### To center the map, make this half of the map width.  
minZoom: -2.5 ### Controls how far away from the map you can zoom out. Hover over the target icon to see the current level.  
maxZoom: 1 ### Controls how far towards the map you can zoom in. Hover over the target icon to see the current level.  
defaultZoom: -2 ### Sets the default zoom level when the map loads. Hover over the target icon to see the current level.  
zoomDelta: 0.5 ### Adjust how much the zoom changes when you zoom in or out.  
unit: mi ### The value displayed when measuring so you know what type of unit is being measure.  
scale: 0.3 ### Real units/px (resolution) of your map  
recenter: false  
darkmode: true ### marker
```















