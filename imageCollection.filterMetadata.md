# imageCollection.filterMetadata      
- creates new image collection that contains only those images from a specified image collection whose values for a specified property bear a specified relationship to a specified value.


## Syntax

#### Javascript
```
newImageCollection = oldImageCollection.filterMetadata ( property, relationship, value )

```

- *newImageCollection* is the new image collection.
- *oldImageCollection* is the specified image collection.
- *property* is the name of the specified property given as a string.
- *relationship* is teh specified relationship given as one of the following strings: "equals" 	"less_than"	"greater_than" "starts_with"	"ends_with"		"contains" "not_equals" 	"not_less_than" 	"not_greater_than" 	"not_starts_with"		"not_ends_with" 	"not_contains"
- *value* is the specified value, given as a string of number. 


## Example

#### Javascript
```javascript
var OldIMAGES    = ee.ImageCollection( 'LC8_L1T_TOA' );    
var NewIMAGES    = OldIMAGES.filterMetadata('CLOUD_COVER','less_than',0.1);
Map.setCenter( -73.015, 41.228, 5);                                                         
Map.addLayer( OldIMAGES, {bands:'B4,B3,B2', min:0, max:0.2, opacity:1.0}, 'Original Images' );
Map.addLayer( NewIMAGES, {bands:'B4,B3,B2', min:0, max:0.2, opacity:1.0}, 'Filtered Images' );
```
