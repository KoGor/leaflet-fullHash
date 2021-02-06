leaflet-fullHash
================

Add dynamic URL hash for Leaflet map (map view and active layers). For those who also lack layers state in [leaflet-hash plugin](https://github.com/mlevans/leaflet-hash). Now you can easily link user to specific map view with certain active layers.

### Demo
You can view a demo of leaflet-fullHash here: [kogor.github.io/leaflet-fullHash](http://kogor.github.io/leaflet-fullHash/index.html).

### Getting started
1. Include [leaflet-fullHash.js](https://github.com/KoGor/leaflet-fullHash/blob/master/leaflet-fullHash.js).

2. Once you have initialized the map (an instance of [L.Map](http://leafletjs.com/reference.html#map-class)), add the following code:

	```javascript
        var osm = L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
            name: 'osm', // this name will be used for the hash-URL
            maxZoom: 19,
            attribution: '© <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>'
        });
        // …
        // Assuming your map instance is in a variable called map
        var allMapLayers = {'Public Name 1': osm,
                            'Public Name 2': leaflet_layer_object2,
                            'Public Name 3': leaflet_layer_object3};
        var hash = new L.Hash(map, allMapLayers);
    ```

### License

MIT License. See [LICENSE](https://github.com/KoGor/leaflet-fullHash/blob/master/LICENSE) for details.
