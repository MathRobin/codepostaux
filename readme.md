# codepostaux

[![Greenkeeper badge](https://badges.greenkeeper.io/MathRobin/codepostaux.svg)](https://greenkeeper.io/)

Give some data about postcodes of France

## Setup

`npm i -S codepostaux`

## Usage

### Include package

`
var CODE_POSTAUX = require('codepostaux');
`

### Search by code Insee (unique ID)

`
CODES_POSTAUX.findByCodeInsee(97128);
// { postcode: '97180', city: 'Sainte-Anne', code_insee: '97128' }
`

### Search by postcode (not unique)

With unique city for a postcode

`CODES_POSTAUX.findByPostCode(75014);
 // [ { postcode: '75014', city: 'Paris', code_insee: '75114' } ]
 `

With numerous cities for only one postcode

`CODES_POSTAUX.findByPostCode(27950);
 // [ { postcode: '27950', city: 'La Chapelle-Réanville', code_insee: '27150' },
      { postcode: '27950', city: 'La Heunière', code_insee: '27336' },
      { postcode: '27950', city: 'Mercey', code_insee: '27399' },
      { postcode: '27950', city: 'Sainte-Colombe-près-Vernon', code_insee: '27525' },
      { postcode: '27950', city: 'Saint-Just', code_insee: '27554' },
      { postcode: '27950', city: 'Saint-Marcel', code_insee: '27562' },
      { postcode: '27950', city: 'Saint-Pierre-d\'Autils', code_insee: '27588' },
      { postcode: '27950', city: 'Saint-Vincent-des-Bois', code_insee: '27612' },
      { postcode: '27950', city: 'Villez-sous-Bailleul', code_insee: '27694' } ]
`

## License

MIT
