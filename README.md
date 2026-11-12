# South-Doyle 2-Mile Food Map

An interactive map of food locations within a 2-mile (3,218.7 m) straight-line radius of
South-Doyle Middle School (3900 Decatur Road, Knoxville, TN 37920), built from
OpenStreetMap data.

The site is fully static: `index.html` plus bundled basemap tiles for the study area.
Open it on GitHub Pages or serve the folder with any static file server.

## What it shows

- 58 OSM records classified as food-related, filtered to the 2-mile radius with a strict
  WGS84 geodesic distance test (no automatic radius expansion).
- Solid dots carry an OSM food category (restaurant, grocery, convenience, etc.);
  hollow dots are potential food sellers that need verification (pharmacies, gas
  stations, dollar stores, bars).
- Filters by category and evidence level, name/address search, and a distance-sorted
  list; each popup links to the source OSM object.

## Data and limitations

- Snapshot retrieved 2026-11-08 from the Overpass API; underlying OSM data as of
  2026-07-28. Counts represent OSM records, not verified operating businesses.
- Straight-line distance is not travel distance. Buildings and areas are placed at the
  bounding-box center OSM returns, so some positions are approximate.
- This is not a complete business directory, and no location has been field-checked
  for current operation.

The data pipeline (Overpass query, classification rules, distance filter, and
regression tests) comes from the companion Jupyter notebook
`South_Doyle_2_Mile_Food_Map_English_Tested.ipynb`.

## Attribution and license

- Map data © [OpenStreetMap contributors](https://www.openstreetmap.org/copyright),
  available under the [Open Database License](https://opendatacommons.org/licenses/odbl/).
- Basemap tiles in `tiles/` were rendered by OpenStreetMap's standard tile layer and are
  included here for the study area only (zooms 13–15, 115 tiles), © OpenStreetMap
  contributors.
- Map rendering by [Leaflet](https://leafletjs.com/) (BSD-2-Clause), loaded from cdnjs.
