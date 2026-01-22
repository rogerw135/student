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
function isPositiveAndOdd(num) {
  let isPositive = num > 0;
  let isOdd = num % 2 !== 0;
  return isPositive && isOdd;
}
<input type="number" id="numInput" placeholder="Enter a number">
<button onclick="runCheck()">Run</button>

<p id="result"></p>
function runCheck() {
  let num = Number(document.getElementById("numInput").value);
  let output = isPositiveAndOdd(num);
  document.getElementById("result").textContent =
    "Result: " + output;
}
console.log(isPositiveAndOdd(7)); // true
console.log(isPositiveAndOdd(8)); // false