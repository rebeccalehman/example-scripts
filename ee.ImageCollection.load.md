# ee.ImageCollection.load
- Creates a new image from an image asset identified by a specified asset ID.

## Syntax

#### Javascript
```
newImageCollection =  ee.ImageCollection.load (  assetID, version )
```

- *newImageCollection* is the new image collection.
- *assetID* is the specified asset ID, given as a string. 
- Optional: *verstion* the version number. Default: -1 (calling for current version)

## Example

#### Javascript
```javascript
var NewIMAGES = ee.ImageCollection.load( 'NOAA/DMSP-OLS/NIGHTTIME_LIGHTS', -1 );
Map.setCenter( 126, 39, 6 );                                          // Korea
Map.addLayer( NewIMAGES, {min:0, max:100, opacity:0.7} );

```
