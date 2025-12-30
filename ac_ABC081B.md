# ABC081B

``` JavaScript
'use strict'

const fs = require('fs');

const input = fs.readFileSync(0, 'utf8').trim().split(/\s+/);
let idx = 0;
const next = () => input[idx++];

const row1 = Number(next()); //回数の取得
let a =[];

for (let i = 0; i < row1; i++){
  a.push(Number(next()));
}
let result = 0; // 結果の数字

// 奇数になるまで実行
while(true){
  if(a.some(v => v % 2 != 0 )){
    break;
  }
  a = a.map(v => v /2);
  result++
}
console.log(result);
``` 