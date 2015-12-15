# block-features

Create GeoJSON polygon features for internal raster tile block

```
Usage: blockfeatures [OPTIONS] RASTER

  Create GeoJSON polygon features of the internal tile blocks for any
  rasterio-supported raster.

  Usage: blockfeatures image.tif > blocks.geojson

  Default, echo a FeatureCollection. Optionally, echo a sequence of
  features.

Options:
  --sequence / --no-sequence  Write a LF-delimited sequence of texts
                              containing individual objects or write a single
                              JSON text containing a feature collection object
                              (the default).
  --rs / --no-rs              Use RS (0x1E) as a prefix for individual texts
                              in a sequence as per http://tools.ietf.org/html
                              /draft-ietf-json-text-sequence-13 (default is
                              False).
  --force                     Force the creation of feautures based on
                              rasterio's block_windows even if the raster is
                              not tiled
  --help                      Show this message and exit.
```

TODO
* [ ] unit tests
* [ ] make rio plugin
* [ ] CI
* [ ] pypi
