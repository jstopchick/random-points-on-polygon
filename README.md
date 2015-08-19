random-points-on-polygon
=============================

Create _n_ number of random points inside a polygon with [TurfJS](http://turfjs.org/)!

## Install

`npm install random-points-on-polygon`

## Usage

#### randomPointsOnPolygon(number, polygon, [properties])

__Params__
- `number`: Integer - the number of random points generated
- `polygon`: Feature<(Polygon|MutiPolygon)> - boundary within points are created
- `properties`: Object [properties={}] - properties object assigned to each random point feature

__Returns__
- `points`: FeatureCollection<Points>

###### Example
```js
var randomPointsOnPolygon = require('random-points-on-polygon');
var turf = require('turf');

var numberOfPoints = 100;
var polygon = turf.random('polygon').features[0];

var points = randomPointsOnPolygon(numberOfPoints, polygon);

// points

// {
//   "type": "FeatureCollection",
//   "features": [
//     {
//       "type": "Feature",
//       "geometry": {
//         "type": "Point",
//         "coordinates": [
//           104.92817194987191,
//           72.68912038906443
//         ]
//       },
//       "properties": {}
//     },
//     {
//       "type": "Feature",
//       "geometry": {
//         "type": "Point",
//         "coordinates": [
//           104.8246191221799,
//           72.02970325707525
//         ]
//       }
//      },
//      ...
//    ]
//  }


```

##Contact

Andy B
