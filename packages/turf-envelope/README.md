# @turf/envelope

# envelope

Takes any number of features and returns a rectangular [Polygon](http://geojson.org/geojson-spec.html#polygon) that encompasses all vertices.

**Parameters**

-   `features` **([Feature](http://geojson.org/geojson-spec.html#feature-objects) \| [FeatureCollection](http://geojson.org/geojson-spec.html#feature-collection-objects))** input features

**Examples**

```javascript
var fc = {
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "properties": {
        "name": "Location A"
      },
      "geometry": {
        "type": "Point",
        "coordinates": [-75.343, 39.984]
      }
    }, {
      "type": "Feature",
      "properties": {
        "name": "Location B"
      },
      "geometry": {
        "type": "Point",
        "coordinates": [-75.833, 39.284]
      }
    }, {
      "type": "Feature",
      "properties": {
        "name": "Location C"
      },
      "geometry": {
        "type": "Point",
        "coordinates": [-75.534, 39.123]
      }
    }
  ]
};

var enveloped = turf.envelope(fc);

var resultFeatures = fc.features.concat(enveloped);
var result = {
  "type": "FeatureCollection",
  "features": resultFeatures
};

//=result
```

Returns **[Feature](http://geojson.org/geojson-spec.html#feature-objects)&lt;[Polygon](http://geojson.org/geojson-spec.html#polygon)>** a rectangular Polygon feature that encompasses all vertices

<!-- This file is automatically generated. Please don't edit it directly:
if you find an error, edit the source file (likely index.js), and re-run
./scripts/generate-readmes in the turf project. -->

---

This module is part of the [Turfjs project](http://turfjs.org/), an open source
module collection dedicated to geographic algorithms. It is maintained in the
[Turfjs/turf](https://github.com/Turfjs/turf) repository, where you can create
PRs and issues.

### Installation

Install this module individually:

```sh
$ npm install @turf/envelope
```

Or install the Turf module that includes it as a function:

```sh
$ npm install @turf/turf
```
