# es6-export-import-object-gotcha

Exporting an object then destructuring the import of that object is invalid.

app.js
```
export default {
  a: 'foo'
}
```

other.js
```
import { a } from './app'
console.log('a', a) //undefined

import * as all from './app'
console.log('All', all) //{default: {a: 'foo'}}
```
