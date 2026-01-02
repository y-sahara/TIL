# ABC087B - Coins
``` JavaScript 
'use strict'

const fs = require('fs');
let s = fs.readFileSync(0, 'utf8').trim().split(/\s+/);
let idx = 0;
const next = () => s[idx++];

const x = Number(next());
const y = Number(next());
const z = Number(next());
const total = Number(next());

let result = 0;
for (let i = 0; i <= x; i++){
  for (let j = 0; j <= y; j++){
    for (let k = 0; k <= z; k++){
      if (total == 500 * i + 100 * j + 50 * k){
        result += 1;
      }
    }
  }
}
console.log(result);
``` 