# ABC085B - Kagami Mochi

``` JavaScript
'use strict'

const fs = require('fs');
let input = fs.readFileSync(0, 'utf8').trim().split(/\s+/);
let idx = 0;
const next = () => Number(input[idx++]);

const n = next();

let arrayA = [];

for(let i = 0; i < n; i++){
  arrayA.push(next());
}
console.log(arrayA);
arrayA = [...new Set(arrayA)];

console.log(arrayA.length);
```