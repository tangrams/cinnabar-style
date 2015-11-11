# Tangram Traditional Style

Give OpenStreetMap data a traditional look using the [Tangram](http://github.com/tangrams/tangram) graphics library and Mapzen's versatile [vector tiles](https://mapzen.com/projects/vector-tiles/). Please use and adapt this open source scene file in your own projects!

**Looking for help?** There is a mini tutorial after the preview image below walking thru [Vector Tiles API key signup](https://github.com/tangrams/traditional-style/blob/gh-pages/README.md#sign-up-for-a-vector-tiles-api-key) and [building a Leaflet map](https://github.com/tangrams/traditional-style/blob/gh-pages/README.md#building-a-leaflet-map-using-tangram-and-this-scene-file) using Tangram and this repo's scene file.

### A family of styles

Mapzen offers the Traditional style in three flavors:

1. **Default** with full labels (this repo) - Including business labels with icons per POI kind.
2. **[Some labels](https://github.com/tangrams/traditional-style-some-labels)** - Streets, cities, and water bodies are labeled and some big parks are named only (no icons). No business labels.
3. **[No labels](https://github.com/tangrams/traditional-style-no-labels)** - Just the lines and polygons.


**Live demo:** http://tangrams.github.io/traditional-style

![tangram traditional style](https://cloud.githubusercontent.com/assets/853051/11080646/c7c6fd26-87ca-11e5-8a04-7316d8721fc4.png)


### Sign up for a Vector Tiles API key

The Tangram scene (style) file [included in this repo](traditional-style-some-labels.yaml) requires a vector tiles source. To use Mapzen's vector tile service you must first obtain a free developer API key. 

**Mapzen Vector Tiles** is a free, shared tile service. As such, there are generous limitations on requests to prevent individual users from degrading the overall system performance.

1. Go to https://mapzen.com/developers.
2. Sign in with your GitHub account. If you have not done this before, you need to agree to the terms first.
3. Create a new key for Vector Tiles, and optionally, give it a project name so you can remember the purpose of the key.
4. Keep the web page open so you can copy the key into your source code later.

### Building a Leaflet map using Tangram and this scene file

1. Reference the [index-demo.html](index-demo.html) file in this repo for how to configure Leaflet with Tangram and the [Mapzen Traditional style scene file](traditional-style-some-labels.yaml). 
2. Looking for a more sophisticated implementation that includes basic search? The main [index.html](index.html) file has a more real world example.
3. Update your copy of the scene file on [line 450](https://github.com/tangrams/traditional-style/blob/gh-pages/traditional-style.yaml#L450) to reference the API key you created in Step 3 in the **Sign up** section above. 

```
url:  //vector.mapzen.com/osm/all/{z}/{x}/{y}.topojson?api_key=vector-tiles-{your-api-key-here}
```


### To run locally

Want to modify the style to fit your needs? Clone or downloaded the repo locally. Then...

Start a web server in the repo's directory:

    python -m SimpleHTTPServer 8000
    
If that doesn't work, try:

    python -m http.server 8000
    
Then navigate to: [http://localhost:8000](http://localhost:8000), which loads the [index.html](index.html) file.