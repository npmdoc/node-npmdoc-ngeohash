# api documentation for  [ngeohash (v0.6.0)](https://github.com/sunng87/node-geohash)  [![npm package](https://img.shields.io/npm/v/npmdoc-ngeohash.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-ngeohash) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-ngeohash.svg)](https://travis-ci.org/npmdoc/node-npmdoc-ngeohash)
#### geohash library for nodejs

[![NPM](https://nodei.co/npm/ngeohash.png?downloads=true)](https://www.npmjs.com/package/ngeohash)

[![apidoc](https://npmdoc.github.io/node-npmdoc-ngeohash/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-ngeohash_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-ngeohash/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-ngeohash/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-ngeohash/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Sun Ning",
        "email": "classicning@gmail.com",
        "url": "http://sunng.info/"
    },
    "bugs": {
        "url": "https://github.com/sunng87/node-geohash/issues"
    },
    "contributors": [
        {
            "name": "Arjun Mehta",
            "email": "arjunmeht@gmail.com",
            "url": "http://www.arjunmehta.net/"
        },
        {
            "name": "Seth Miller",
            "email": "seth@four43.com",
            "url": "http://www.four43.com"
        },
        {
            "name": "Zhu Zhe",
            "email": "zhuzhe1983@gmail.com"
        }
    ],
    "dependencies": {},
    "description": "geohash library for nodejs",
    "devDependencies": {
        "assert": ">=1.0",
        "nodeunit": ">=0.8"
    },
    "directories": {},
    "dist": {
        "shasum": "329713e9e73d1f1a46d92aab0b94adb94533f687",
        "tarball": "https://registry.npmjs.org/ngeohash/-/ngeohash-0.6.0.tgz"
    },
    "engines": {
        "node": ">=v0.2.0"
    },
    "homepage": "https://github.com/sunng87/node-geohash",
    "keywords": [
        "geohash",
        "uint64",
        "geohasher",
        "geocode",
        "geolocation"
    ],
    "license": "MIT",
    "main": "./main",
    "maintainers": [
        {
            "name": "sunng",
            "email": "classicning@gmail.com"
        }
    ],
    "name": "ngeohash",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "url": "git+https://github.com/sunng87/node-geohash.git"
    },
    "scripts": {
        "test": "nodeunit tests/test.js"
    },
    "version": "0.6.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module ngeohash](#apidoc.module.ngeohash)
1.  [function <span class="apidocSignatureSpan">ngeohash.</span>bboxes (minLat, minLon, maxLat, maxLon, numberOfChars)](#apidoc.element.ngeohash.bboxes)
1.  [function <span class="apidocSignatureSpan">ngeohash.</span>bboxes_int (minLat, minLon, maxLat, maxLon, bitDepth)](#apidoc.element.ngeohash.bboxes_int)
1.  [function <span class="apidocSignatureSpan">ngeohash.</span>decode (hashString)](#apidoc.element.ngeohash.decode)
1.  [function <span class="apidocSignatureSpan">ngeohash.</span>decode_bbox (hash_string)](#apidoc.element.ngeohash.decode_bbox)
1.  [function <span class="apidocSignatureSpan">ngeohash.</span>decode_bbox_int (hashInt, bitDepth)](#apidoc.element.ngeohash.decode_bbox_int)
1.  [function <span class="apidocSignatureSpan">ngeohash.</span>decode_bbox_uint64 (hashInt, bitDepth)](#apidoc.element.ngeohash.decode_bbox_uint64)
1.  [function <span class="apidocSignatureSpan">ngeohash.</span>decode_int (hash_int, bitDepth)](#apidoc.element.ngeohash.decode_int)
1.  [function <span class="apidocSignatureSpan">ngeohash.</span>decode_uint64 (hash_int, bitDepth)](#apidoc.element.ngeohash.decode_uint64)
1.  [function <span class="apidocSignatureSpan">ngeohash.</span>encode (latitude, longitude, numberOfChars)](#apidoc.element.ngeohash.encode)
1.  [function <span class="apidocSignatureSpan">ngeohash.</span>encode_int (latitude, longitude, bitDepth)](#apidoc.element.ngeohash.encode_int)
1.  [function <span class="apidocSignatureSpan">ngeohash.</span>encode_uint64 (latitude, longitude, bitDepth)](#apidoc.element.ngeohash.encode_uint64)
1.  [function <span class="apidocSignatureSpan">ngeohash.</span>neighbor (hashString, direction)](#apidoc.element.ngeohash.neighbor)
1.  [function <span class="apidocSignatureSpan">ngeohash.</span>neighbor_int (hash_int, direction, bitDepth)](#apidoc.element.ngeohash.neighbor_int)
1.  [function <span class="apidocSignatureSpan">ngeohash.</span>neighbors (hash_string)](#apidoc.element.ngeohash.neighbors)
1.  [function <span class="apidocSignatureSpan">ngeohash.</span>neighbors_int (hash_int, bitDepth)](#apidoc.element.ngeohash.neighbors_int)
1.  string <span class="apidocSignatureSpan">ngeohash.</span>ENCODE_AUTO



# <a name="apidoc.module.ngeohash"></a>[module ngeohash](#apidoc.module.ngeohash)

#### <a name="apidoc.element.ngeohash.bboxes"></a>[function <span class="apidocSignatureSpan">ngeohash.</span>bboxes (minLat, minLon, maxLat, maxLon, numberOfChars)](#apidoc.element.ngeohash.bboxes)
- description and source-code
```javascript
bboxes = function (minLat, minLon, maxLat, maxLon, numberOfChars) {
  numberOfChars = numberOfChars || 9;

  var hashSouthWest = encode(minLat, minLon, numberOfChars);
  var hashNorthEast = encode(maxLat, maxLon, numberOfChars);

  var latLon = decode(hashSouthWest);

  var perLat = latLon.error.latitude * 2;
  var perLon = latLon.error.longitude * 2;

  var boxSouthWest = decode_bbox(hashSouthWest);
  var boxNorthEast = decode_bbox(hashNorthEast);

  var latStep = Math.round((boxNorthEast[0] - boxSouthWest[0]) / perLat);
  var lonStep = Math.round((boxNorthEast[1] - boxSouthWest[1]) / perLon);

  var hashList = [];

  for (var lat = 0; lat <= latStep; lat++) {
    for (var lon = 0; lon <= lonStep; lon++) {
      hashList.push(neighbor(hashSouthWest, [lat, lon]));
    }
  }

  return hashList;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ngeohash.bboxes_int"></a>[function <span class="apidocSignatureSpan">ngeohash.</span>bboxes_int (minLat, minLon, maxLat, maxLon, bitDepth)](#apidoc.element.ngeohash.bboxes_int)
- description and source-code
```javascript
bboxes_int = function (minLat, minLon, maxLat, maxLon, bitDepth){
    bitDepth = bitDepth || 52;

    var hashSouthWest = encode_int(minLat, minLon, bitDepth);
    var hashNorthEast = encode_int(maxLat, maxLon, bitDepth);

    var latlon = decode_int(hashSouthWest, bitDepth);

    var perLat = latlon.error.latitude * 2;
    var perLon = latlon.error.longitude * 2;

    var boxSouthWest = decode_bbox_int(hashSouthWest, bitDepth);
    var boxNorthEast = decode_bbox_int(hashNorthEast, bitDepth);

    var latStep = Math.round((boxNorthEast[0] - boxSouthWest[0])/perLat);
    var lonStep = Math.round((boxNorthEast[1] - boxSouthWest[1])/perLon);

    var hashList = [];

    for(var lat = 0; lat <= latStep; lat++){
        for(var lon = 0; lon <= lonStep; lon++){
            hashList.push(neighbor_int(hashSouthWest,[lat, lon], bitDepth));
        }
    }

    return hashList;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ngeohash.decode"></a>[function <span class="apidocSignatureSpan">ngeohash.</span>decode (hashString)](#apidoc.element.ngeohash.decode)
- description and source-code
```javascript
decode = function (hashString) {
  var bbox = decode_bbox(hashString);
  var lat = (bbox[0] + bbox[2]) / 2;
  var lon = (bbox[1] + bbox[3]) / 2;
  var latErr = bbox[2] - lat;
  var lonErr = bbox[3] - lon;
  return {latitude: lat, longitude: lon,
          error: {latitude: latErr, longitude: lonErr}};
}
```
- example usage
```shell
...

## Usage

'''javascript
var geohash = require('ngeohash');
console.log(geohash.encode(37.8324, 112.5584));
// prints ww8p1r4t8
var latlon = geohash.decode('ww8p1r4t8');
console.log(latlon.latitude);
console.log(latlon.longitude);
'''


## Basic Methods
...
```

#### <a name="apidoc.element.ngeohash.decode_bbox"></a>[function <span class="apidocSignatureSpan">ngeohash.</span>decode_bbox (hash_string)](#apidoc.element.ngeohash.decode_bbox)
- description and source-code
```javascript
decode_bbox = function (hash_string) {
  var isLon = true,
  maxLat = 90,
  minLat = -90,
  maxLon = 180,
  minLon = -180,
  mid;

  var hashValue = 0;
  for (var i = 0, l = hash_string.length; i < l; i++) {
    var code = hash_string[i].toLowerCase();
    hashValue = BASE32_CODES_DICT[code];

    for (var bits = 4; bits >= 0; bits--) {
      var bit = (hashValue >> bits) & 1;
      if (isLon) {
        mid = (maxLon + minLon) / 2;
        if (bit === 1) {
          minLon = mid;
        } else {
          maxLon = mid;
        }
      } else {
        mid = (maxLat + minLat) / 2;
        if (bit === 1) {
          minLat = mid;
        } else {
          maxLat = mid;
        }
      }
      isLon = !isLon;
    }
  }
  return [minLat, minLon, maxLat, maxLon];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ngeohash.decode_bbox_int"></a>[function <span class="apidocSignatureSpan">ngeohash.</span>decode_bbox_int (hashInt, bitDepth)](#apidoc.element.ngeohash.decode_bbox_int)
- description and source-code
```javascript
decode_bbox_int = function (hashInt, bitDepth) {

  bitDepth = bitDepth || 52;

  var maxLat = 90,
  minLat = -90,
  maxLon = 180,
  minLon = -180;

  var latBit = 0, lonBit = 0;
  var step = bitDepth / 2;

  for (var i = 0; i < step; i++) {

    lonBit = get_bit(hashInt, ((step - i) * 2) - 1);
    latBit = get_bit(hashInt, ((step - i) * 2) - 2);

    if (latBit === 0) {
      maxLat = (maxLat + minLat) / 2;
    }
    else {
      minLat = (maxLat + minLat) / 2;
    }

    if (lonBit === 0) {
      maxLon = (maxLon + minLon) / 2;
    }
    else {
      minLon = (maxLon + minLon) / 2;
    }
  }
  return [minLat, minLon, maxLat, maxLon];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ngeohash.decode_bbox_uint64"></a>[function <span class="apidocSignatureSpan">ngeohash.</span>decode_bbox_uint64 (hashInt, bitDepth)](#apidoc.element.ngeohash.decode_bbox_uint64)
- description and source-code
```javascript
decode_bbox_uint64 = function (hashInt, bitDepth) {

  bitDepth = bitDepth || 52;

  var maxLat = 90,
  minLat = -90,
  maxLon = 180,
  minLon = -180;

  var latBit = 0, lonBit = 0;
  var step = bitDepth / 2;

  for (var i = 0; i < step; i++) {

    lonBit = get_bit(hashInt, ((step - i) * 2) - 1);
    latBit = get_bit(hashInt, ((step - i) * 2) - 2);

    if (latBit === 0) {
      maxLat = (maxLat + minLat) / 2;
    }
    else {
      minLat = (maxLat + minLat) / 2;
    }

    if (lonBit === 0) {
      maxLon = (maxLon + minLon) / 2;
    }
    else {
      minLon = (maxLon + minLon) / 2;
    }
  }
  return [minLat, minLon, maxLat, maxLon];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ngeohash.decode_int"></a>[function <span class="apidocSignatureSpan">ngeohash.</span>decode_int (hash_int, bitDepth)](#apidoc.element.ngeohash.decode_int)
- description and source-code
```javascript
decode_int = function (hash_int, bitDepth) {
  var bbox = decode_bbox_int(hash_int, bitDepth);
  var lat = (bbox[0] + bbox[2]) / 2;
  var lon = (bbox[1] + bbox[3]) / 2;
  var latErr = bbox[2] - lat;
  var lonErr = bbox[3] - lon;
  return {latitude: lat, longitude: lon,
          error: {latitude: latErr, longitude: lonErr}};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ngeohash.decode_uint64"></a>[function <span class="apidocSignatureSpan">ngeohash.</span>decode_uint64 (hash_int, bitDepth)](#apidoc.element.ngeohash.decode_uint64)
- description and source-code
```javascript
decode_uint64 = function (hash_int, bitDepth) {
  var bbox = decode_bbox_int(hash_int, bitDepth);
  var lat = (bbox[0] + bbox[2]) / 2;
  var lon = (bbox[1] + bbox[3]) / 2;
  var latErr = bbox[2] - lat;
  var lonErr = bbox[3] - lon;
  return {latitude: lat, longitude: lon,
          error: {latitude: latErr, longitude: lonErr}};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ngeohash.encode"></a>[function <span class="apidocSignatureSpan">ngeohash.</span>encode (latitude, longitude, numberOfChars)](#apidoc.element.ngeohash.encode)
- description and source-code
```javascript
encode = function (latitude, longitude, numberOfChars) {
  if (numberOfChars === ENCODE_AUTO) {
    if (typeof(latitude) === 'number' || typeof(longitude) === 'number') {
      throw new Error('string notation required for auto precision.');
    }
    var decSigFigsLat = latitude.split('.')[1].length;
    var decSigFigsLong = longitude.split('.')[1].length;
    var numberOfSigFigs = Math.max(decSigFigsLat, decSigFigsLong);
    numberOfChars = SIGFIG_HASH_LENGTH[numberOfSigFigs];
  } else if (numberOfChars === undefined) {
    numberOfChars = 9;
  }

  var chars = [],
  bits = 0,
  bitsTotal = 0,
  hash_value = 0,
  maxLat = 90,
  minLat = -90,
  maxLon = 180,
  minLon = -180,
  mid;
  while (chars.length < numberOfChars) {
    if (bitsTotal % 2 === 0) {
      mid = (maxLon + minLon) / 2;
      if (longitude > mid) {
        hash_value = (hash_value << 1) + 1;
        minLon = mid;
      } else {
        hash_value = (hash_value << 1) + 0;
        maxLon = mid;
      }
    } else {
      mid = (maxLat + minLat) / 2;
      if (latitude > mid) {
        hash_value = (hash_value << 1) + 1;
        minLat = mid;
      } else {
        hash_value = (hash_value << 1) + 0;
        maxLat = mid;
      }
    }

    bits++;
    bitsTotal++;
    if (bits === 5) {
      var code = BASE32_CODES[hash_value];
      chars.push(code);
      bits = 0;
      hash_value = 0;
    }
  }
  return chars.join('');
}
```
- example usage
```shell
...
'''


## Usage

'''javascript
var geohash = require('ngeohash');
console.log(geohash.encode(37.8324, 112.5584));
// prints ww8p1r4t8
var latlon = geohash.decode('ww8p1r4t8');
console.log(latlon.latitude);
console.log(latlon.longitude);
'''
...
```

#### <a name="apidoc.element.ngeohash.encode_int"></a>[function <span class="apidocSignatureSpan">ngeohash.</span>encode_int (latitude, longitude, bitDepth)](#apidoc.element.ngeohash.encode_int)
- description and source-code
```javascript
encode_int = function (latitude, longitude, bitDepth) {

  bitDepth = bitDepth || 52;

  var bitsTotal = 0,
  maxLat = 90,
  minLat = -90,
  maxLon = 180,
  minLon = -180,
  mid,
  combinedBits = 0;

  while (bitsTotal < bitDepth) {
    combinedBits *= 2;
    if (bitsTotal % 2 === 0) {
      mid = (maxLon + minLon) / 2;
      if (longitude > mid) {
        combinedBits += 1;
        minLon = mid;
      } else {
        maxLon = mid;
      }
    } else {
      mid = (maxLat + minLat) / 2;
      if (latitude > mid) {
        combinedBits += 1;
        minLat = mid;
      } else {
        maxLat = mid;
      }
    }
    bitsTotal++;
  }
  return combinedBits;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ngeohash.encode_uint64"></a>[function <span class="apidocSignatureSpan">ngeohash.</span>encode_uint64 (latitude, longitude, bitDepth)](#apidoc.element.ngeohash.encode_uint64)
- description and source-code
```javascript
encode_uint64 = function (latitude, longitude, bitDepth) {

  bitDepth = bitDepth || 52;

  var bitsTotal = 0,
  maxLat = 90,
  minLat = -90,
  maxLon = 180,
  minLon = -180,
  mid,
  combinedBits = 0;

  while (bitsTotal < bitDepth) {
    combinedBits *= 2;
    if (bitsTotal % 2 === 0) {
      mid = (maxLon + minLon) / 2;
      if (longitude > mid) {
        combinedBits += 1;
        minLon = mid;
      } else {
        maxLon = mid;
      }
    } else {
      mid = (maxLat + minLat) / 2;
      if (latitude > mid) {
        combinedBits += 1;
        minLat = mid;
      } else {
        maxLat = mid;
      }
    }
    bitsTotal++;
  }
  return combinedBits;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ngeohash.neighbor"></a>[function <span class="apidocSignatureSpan">ngeohash.</span>neighbor (hashString, direction)](#apidoc.element.ngeohash.neighbor)
- description and source-code
```javascript
neighbor = function (hashString, direction) {
  var lonLat = decode(hashString);
  var neighborLat = lonLat.latitude
    + direction[0] * lonLat.error.latitude * 2;
  var neighborLon = lonLat.longitude
    + direction[1] * lonLat.error.longitude * 2;
  return encode(neighborLat, neighborLon, hashString.length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ngeohash.neighbor_int"></a>[function <span class="apidocSignatureSpan">ngeohash.</span>neighbor_int (hash_int, direction, bitDepth)](#apidoc.element.ngeohash.neighbor_int)
- description and source-code
```javascript
neighbor_int = function (hash_int, direction, bitDepth) {
    bitDepth = bitDepth || 52;
    var lonlat = decode_int(hash_int, bitDepth);
    var neighbor_lat = lonlat.latitude + direction[0] * lonlat.error.latitude * 2;
    var neighbor_lon = lonlat.longitude + direction[1] * lonlat.error.longitude * 2;
    return encode_int(neighbor_lat, neighbor_lon, bitDepth);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ngeohash.neighbors"></a>[function <span class="apidocSignatureSpan">ngeohash.</span>neighbors (hash_string)](#apidoc.element.ngeohash.neighbors)
- description and source-code
```javascript
neighbors = function (hash_string){

    var hashstringLength = hash_string.length;

    var lonlat = decode(hash_string);
    var lat = lonlat.latitude;
    var lon = lonlat.longitude;
    var latErr = lonlat.error.latitude * 2;
    var lonErr = lonlat.error.longitude * 2;

    var neighbor_lat,
        neighbor_lon;

    var neighborHashList = [
                            encodeNeighbor(1,0),
                            encodeNeighbor(1,1),
                            encodeNeighbor(0,1),
                            encodeNeighbor(-1,1),
                            encodeNeighbor(-1,0),
                            encodeNeighbor(-1,-1),
                            encodeNeighbor(0,-1),
                            encodeNeighbor(1,-1)
                            ];

    function encodeNeighbor(neighborLatDir, neighborLonDir){
        neighbor_lat = lat + neighborLatDir * latErr;
        neighbor_lon = lon + neighborLonDir * lonErr;
        return encode(neighbor_lat, neighbor_lon, hashstringLength);
    }

    return neighborHashList;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ngeohash.neighbors_int"></a>[function <span class="apidocSignatureSpan">ngeohash.</span>neighbors_int (hash_int, bitDepth)](#apidoc.element.ngeohash.neighbors_int)
- description and source-code
```javascript
neighbors_int = function (hash_int, bitDepth){

    bitDepth = bitDepth || 52;

    var lonlat = decode_int(hash_int, bitDepth);
    var lat = lonlat.latitude;
    var lon = lonlat.longitude;
    var latErr = lonlat.error.latitude * 2;
    var lonErr = lonlat.error.longitude * 2;

    var neighbor_lat,
        neighbor_lon;

    var neighborHashIntList = [
                            encodeNeighbor_int(1,0),
                            encodeNeighbor_int(1,1),
                            encodeNeighbor_int(0,1),
                            encodeNeighbor_int(-1,1),
                            encodeNeighbor_int(-1,0),
                            encodeNeighbor_int(-1,-1),
                            encodeNeighbor_int(0,-1),
                            encodeNeighbor_int(1,-1)
                            ];

    function encodeNeighbor_int(neighborLatDir, neighborLonDir){
        neighbor_lat = lat + neighborLatDir * latErr;
        neighbor_lon = lon + neighborLonDir * lonErr;
        return encode_int(neighbor_lat, neighbor_lon, bitDepth);
    }

    return neighborHashIntList;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
