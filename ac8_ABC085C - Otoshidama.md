# ABC085C - Otoshidama

``` JavaScript 
'use strict'

const fs = require('fs');
const input = fs.readFileSync(0, 'utf8').trim().split(/\s+/);
let idx =0;
const next = () => Number(input[idx++]);

const n = next();
const Y = next();

for (let x = 0; x <= n; x++){
  for (let y = 0; y <= (n - x); y++) {
    let z = n - x - y;
    if (10000 * x + 5000 * y + 1000 * z == Y){
      console.log(`${x} ${y} ${z}`)
      return;
    }
  }
}
console.log('-1 -1 -1');
```