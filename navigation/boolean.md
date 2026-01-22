---
layout: page
title: Boolean
permalink: /boolean/
comments: true
---
function isPositiveAndOdd(num) {
  let isPositive = num > 0;
  let isOdd = num % 2 !== 0;
  return isPositive && isOdd;
}

console.log(isPositiveAndOdd(7)); // true
console.log(isPositiveAndOdd(8)); // false
