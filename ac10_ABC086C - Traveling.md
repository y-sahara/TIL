# ABC086C - Traveling

``` JavaScript 
'use strict'

const fs = require('fs');
let s = fs.readFileSync(0, 'utf8').trim().split(/\s+/);
let idx = 0;
const next = () => Number(s[idx++]);

const n = next();

const t = [0]; // 時間軸
const x = [0]; // x軸
const y = [0]; // y軸

for (let i = 1; i <= n; i++){
  t[i] = next();
  x[i] = next();
  y[i] = next();
  
  let a = t[i] - t[i - 1];
  let b = Math.abs(x[i] - x[i - 1]);
  let c = Math.abs(y[i] - y[i - 1]);
  if ( (a % 2 != 0 && ((b + c) % 2 == 0) )
  || a < (b + c)
  ){
    console.log('No');
    return;
  }
}
console.log('Yes');
```