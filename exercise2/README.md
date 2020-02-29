# Vector tiles with Mapbox GL JS

- Head to http://bit.ly/mapbox-gl-js-basic in a new tab.
- View the page’s source code- right-click anywhere, then click View Page Source.

### Initialize your first Mapbox GL JS map
1. Fire up your text editor. In this class, we’ll be using Visual Studio Code (aka “VS Code”). Web mappers rely heavily on their text editors to get stuff done. We’re going to use ours a lot during this class.
2. In VS Code, add the folder containing all of today’s class materials to your Workspace (you should have downloaded this from GitHub already): From the File menu, click Add Folder to Workspace, then navigate to today’s class folder on your computer and click Add.
3. Open output2.html

![image](images/slide74.png)
```html
<!-- Add Mapbox GL JS JavaScript file -->
<script src='https://api.tiles.mapbox.com/mapbox-gl-js/v1.5.0/mapbox-gl.js'></script>

<!-- Add in the Mapbox GL JS CSS file -->
<link href='https://api.tiles.mapbox.com/mapbox-gl-js/v1.5.0/mapbox-gl.css' rel='stylesheet' />
```

![image](images/slide75.png)

Inside the style tag (Lines 11-13):
```html
       body {
           margin: 0;
           padding: 0;
       }
       #mapId {
           position: absolute;
           top: 0;
           bottom: 0;
           width: 100%;
       }
```
![image](images/slide76.png)

```html
 <div id="mapId"></div>
```


![image](images/slide77.png)
#### Grab your default Mapbox Access Token [here](https://account.mapbox.com/access-tokens/)

```html
<script>
// Mapbox GL JS requires a token
mapboxgl.accessToken = 'your token goes here’;
      
// Initialize the map
var map = new mapboxgl.Map({
container: 'mapId', 
style: 'mapbox://styles/mapbox/streets-v11', 
center: [-122.420790, 37.754700], 
zoom: 14 
});
</script>
```

### What’s different about Mapbox GL JS vs Leaflet?
![image](images/slide80.png)

## Additional Resources
- [Mapbox GL JS documentation](https://docs.mapbox.com/mapbox-gl-js/api/)
