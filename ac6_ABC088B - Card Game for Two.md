# ABC088B - Card Game for Two
``` JavaScript 
'use strict'

const fs = require('fs');
let s = fs.readFileSync(0, 'utf8').trim().split(/\s+/);
let idx = 0;
const next = () => Number(s[idx++]);

const n = next();
let alice = 0;
let bob = 0;

let a = [];
for (let i = 0; i < n; i++){
  a.push(next());
}
a = a.sort((a, b) => b- a); // 降順に並べる

for (let i = 0; i < a.length; i++){
  if (i % 2 == 0){
    alice += a[i];
  } else {
    bob += a[i];
  }
}

console.log(alice -bob);
``` 