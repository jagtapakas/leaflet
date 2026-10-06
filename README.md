# Leaflet Map

Angular 19 + Leaflet world map example.

## Run

```bash
npm install
npm start
```

Open the URL printed by Angular CLI (normally `http://localhost:4200`).

## What was fixed

- Fixed the Leaflet component stylesheet reference from `.css` to `.scss`.
- Removed the invalid/unused `assets/world.geojson` TypeScript import.
- Kept the bundled `geo.ts` GeoJSON data as the map boundary source.
- Made `MapComponent` explicitly standalone and imported `CommonModule` for `*ngIf`.
- Removed the unused NgModule/router setup from this map-only application.
- Added Leaflet cleanup in `ngOnDestroy`.
- Added `invalidateSize()` handling for layouts that resize after initialization.
- Prevented duplicate Leaflet initialization during development/hot reload.
- Added a Back button after selecting a country.
- Added basic bounds validation before zooming.

## Notes

The map tiles come from OpenStreetMap, so the browser needs internet access to display the tile imagery. The country boundaries are bundled locally.
