# Slovenské pranostiky (slovak only) 🇸🇰
> DEV EDITION

# Obsah
* [Data](#data)
* [API](#api)
  * [Aplikácia](#endpoint) 
* [Referencie](#referencie)

## Data
`src/data.json`

### Príklad

> Pranostiky na 15. júl

```javascript
// data[MONTH_INDEX][DAY_IN_MONTH] => string[];

data["6"]["15"];
/*
[
    "Rozoslanie apoštolov rozhadzuje krížiky.",
    "Na deň Rozoslania apoštolov poprcháva, to Magdaléna /22.7/ svojho pána",
    "Ak prší na deň Rozoslania apoštolov, bude drahota.",
    "Július mokrý a studený, znivočí nám všetko oseví."
];
*/
```

## API

### Endpoint
[https://slovenske-pranostiky-api.herokuapp.com/](https://slovenske-pranostiky-api.herokuapp.com/)

### Routes

| ROUTE | METHOD |
|:-------------|:-------------|
| `/` | **GET** |
| `/:month` | **GET** |
| `/:month/:day` | **GET** |

### Interface
```javascript
month: 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12;
day: number;
```

### Príklad
> Pranostiky na 15. júl

```javascript
fetch('https://slovenske-pranostiky-api.herokuapp.com/7/15').then(...);
```

