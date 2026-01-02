# ABC083B - Some Sums
``` JavaScript 
'use strict';

const fs = require('fs');
const s = fs.readFileSync(0, 'utf8').trim().split(/\s+/);
let idx = 0;
const next = () => s[idx++];

const n = Number(next());
const a = Number(next());
const b = Number(next());

let result = 0;

for (let i = 0; i <= n; i++) {
  let sum = 0;
  for (const ch of String(i)) {
    sum += Number(ch);
  }
  if (a <= sum && sum <= b) {
    result += i;
  }
}

console.log(result);
```