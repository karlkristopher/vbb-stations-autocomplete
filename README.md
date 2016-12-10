# vbb-stations-autocomplete

*vbb-stations-autocomplete* provides a **stations search for the Berlin Brandenburg public transport service (VBB)**. It pulls its data from [`vbb-static`](https://github.com/derhuerst/vbb-static).

[![npm version](https://img.shields.io/npm/v/vbb-stations-autocomplete.svg)](https://www.npmjs.com/package/vbb-stations-autocomplete)
[![build status](https://img.shields.io/travis/derhuerst/vbb-stations-autocomplete.svg)](https://travis-ci.org/derhuerst/vbb-stations-autocomplete)
[![dependency status](https://img.shields.io/david/derhuerst/vbb-stations-autocomplete.svg)](https://david-dm.org/derhuerst/vbb-stations-autocomplete)
[![dev dependency status](https://img.shields.io/david/dev/derhuerst/vbb-stations-autocomplete.svg)](https://david-dm.org/derhuerst/vbb-stations-autocomplete#info=devDependencies)
![ISC-licensed](https://img.shields.io/github/license/derhuerst/vbb-stations-autocomplete.svg)
[![gitter channel](https://badges.gitter.im/derhuerst/vbb-rest.svg)](https://gitter.im/derhuerst/vbb-rest)


## Installing

```shell
npm install vbb-stations-autocomplete
```


## Usage

```javascript
const autocomplete = require('vbb-stations-autocomplete')
autocomplete('Seestr', 3)   // limit to results 3
```

returns

```javascript
[
    {
        id: '900000009105',
		// Taken from `vbb-static`.
        name: 'Seestr./Amrumer Str.',
        weight: 2625.75, tokens: 4,
		// Based on how much of the station's name is mached
		// by the search query. Also, the station's weight is
		// taken into account.
        relevance: 155.31927802111366
    }, {
        id: '900000009103',
        name: 'U Seestr.',
        weight: 6263.75, tokens: 3,
        relevance: 120.8942375246507
    }, {
        id: '900000019103',
        name: 'Seestr./Beusselstr.',
        weight: 1549.5, tokens: 4,
        relevance: 119.31484086231687
    }
]
```


## Contributing

If you **have a question**, **found a bug** or want to **propose a feature**, have a look at [the issues page](https://github.com/derhuerst/vbb-stations-autocomplete/issues).
