# 🇧🇷 Brazil Geo JSON

This repository provides simple and lightweight **GeoJSON** files representing Brazil’s geographic divisions: **regions** and **states**.

## 📁 Contents

- **`br_regions.json`** — GeoJSON for Brazil’s five major regions  
  (*Norte, Nordeste, Sudeste, Sul, Centro-Oeste*)
- **`br_states.json`** — GeoJSON for all **26 states** + **Federal District**

These files are suitable for use in mapping libraries, dashboards, GIS tools, and spatial analysis.

## 🧭 Purpose

This repository aims to provide:

- Clean, ready-to-use GeoJSON boundaries of Brazil  
- A lightweight dataset for web mapping (Leaflet, Mapbox, etc.)  
- A convenient base layer for data visualizations and geographic applications  

## 🚀 How to Use

Clone the repo:

```bash
git clone https://github.com/tiagoturra/geo.git
```

Load the GeoJSON in your project:

### JavaScript (Leaflet)
```javascript
fetch('br_states.json')
  .then(res => res.json())
  .then(data => L.geoJSON(data).addTo(map));
```

### Python (GeoPandas)
```python
import geopandas as gpd

states = gpd.read_file("br_states.json")
regions = gpd.read_file("br_regions.json")
```

## 🌱 Contributing

Contributions are welcome!

You may contribute by:
* Adding new geographic layers (e.g., municipalities)
* Updating geometry precision
* Adding TopoJSON versions
* Improving documentation

Before submitting a PR:
* Validate GeoJSON files using a linter
* Ensure coordinates follow standard EPSG:4326
* Document your changes clearly

## 🛣️ Possible Future Enhancements

* Add municipality boundaries
* Provide TopoJSON for file-size optimization
* Add simplified vs detailed geometry variants
* Publish releases with versioned datasets

## 📄 License (MIT)

MIT License

Copyright (c) 2025 Tiago Turra

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
