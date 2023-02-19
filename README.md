### This solution for Sales by Match which is socks merchant in Hacker Rank
My Initial solution is
```
function sockMerchant(n, ar) {
const countObj = {};  // Here assume all duplicate Elements
for (const iterator of ar) {
  countObj[iterator] = countObj[iterator] ? countObj[iterator] + 1 : 1;
}
const filteredObj = {};  // Filtering element if which isn't only 1 element 
& if above 1 element found & even it's odd let's minus by 1
for (const key in countObj) {
  if (countObj[key] > 1) {
    filteredObj[key] = countObj[key];
  if (filteredObj[key] % 2 !== 0) {
      filteredObj[key] = filteredObj[key] - 1;
    }
  }
}
let final = 0;  // Final assume all pairs
for (const key1 in filteredObj) {
  final += filteredObj[key1] / 2;
}
return final;
}
```