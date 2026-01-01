``` JavaScript 
'use strict'

const fs = require('fs');
let s = fs.readFileSync(0, 'utf8').trim();

s = s.split('').reverse().join('');

const words = [
  'dream',
  'dreamer',
  'erase',
  'eraser'].map(w => w.split('').reverse().join(''))
  .sort((a, b) => b.length - a.length);
  
let i = 0;
while(i < s.length){
  let matched = false;
  
  for (const w of words){
    if(s.startsWith(w, i)){
      i += w.length;
      matched = true;
      break;
    }
  }
  
  if (!matched) {
    console.log('NO');
    return;
  }
}

console.log('YES');
``` 