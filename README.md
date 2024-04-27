# @zibuthe7j11/ipsam-atque-vero
---

[![Build Status](https://travis-ci.org/aligay/@zibuthe7j11/ipsam-atque-vero.svg?branch=master)](https://travis-ci.org/aligay/@zibuthe7j11/ipsam-atque-vero/branches)
[![codecov](https://codecov.io/gh/aligay/@zibuthe7j11/ipsam-atque-vero/branch/master/graph/badge.svg)](https://codecov.io/gh/aligay/@zibuthe7j11/ipsam-atque-vero)
[![dependencies Status](https://david-dm.org/aligay/@zibuthe7j11/ipsam-atque-vero/status.svg)](https://david-dm.org/aligay/@zibuthe7j11/ipsam-atque-vero)
[![devDependencies Status](https://david-dm.org/aligay/@zibuthe7j11/ipsam-atque-vero/dev-status.svg)](https://david-dm.org/aligay/@zibuthe7j11/ipsam-atque-vero?type=dev)

## install
```
npm install @zibuthe7j11/ipsam-atque-vero
```
## use
```
import safeTrim from '@zibuthe7j11/ipsam-atque-vero'
safeTrim('    a      b  ')
```

## remove Invisible spaces

```
let str = '  "a":1    a \r\n\r\t  ᠎             　b       '
let ret = safeTrim(str)
expect(ret).toEqual('"a":1    a\n\nb')
```

## convert CR CR-LR into LR
```
a\r\n\r\nb  => 'a\n\nb'
a\r\rb => 'a\n\nb'
a\r\r\nb => 'a\n\nb'
```

## remove BOM
```
JSON.parse('﻿{"a":1}') // ❗️Error because BOM

JSON.parse(safeTrim('﻿{"a":1}')) // ✅
```


## more feature
[more feature](spec/test_spec.js)
