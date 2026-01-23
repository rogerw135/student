---
layout: page
title: Iteration
permalink: /iterations/
comments: true
---
let fruits = ["Heart Shaped Herb", "Yami Yami no Mi", "Gomu Gomu no Mi"];

// ---------------- Loop 1: Forward (basic counting loop)
// Condition: increases while less than array length
for (let i = 0; i < fruits.length; i++) {
  console.log("Forward:", fruits[i]);
}

console.log("----------------");

// ---------------- Loop 2: Backward
// Condition: decreases while >= 0
for (let i = fruits.length - 1; i >= 0; i--) {
  console.log("Backward:", fruits[i]);
}

console.log("----------------");

// ---------------- Loop 3: for...of with IF condition
// Condition inside loop filters results
for (let fruit of fruits) {
  if (fruit.includes("no Mi")) {   // only Devil Fruits
    console.log("Devil Fruit:", fruit);
  }
}

console.log("----------------");

// ---------------- Loop 4: while loop
// Condition: runs until a name contains "Gomu"
let index = 0;
while (index < fruits.length && !fruits[index].includes("Gomu")) {
  console.log("While Loop Fruit:", fruits[index]);
  index++;
}

console.log("----------------");

// ---------------- Loop 5: do...while loop
// Condition checked AFTER first run
let count = 0;
do {
  console.log("Do-While Fruit:", fruits[count]);
  count++;
} while (count < fruits.length);
function runLoops() {
  let fruits = ["Heart Shaped Herb", "Yami Yami no Mi", "Gomu Gomu no Mi"];
  let output = "";

  // Loop 1 Forward
  for (let i = 0; i < fruits.length; i++) {
    output += "Forward: " + fruits[i] + "\n";
  }

  output += "----------------\n";

  // Loop 2 Backward
  for (let i = fruits.length - 1; i >= 0; i--) {
    output += "Backward: " + fruits[i] + "\n";
  }

  output += "----------------\n";

  // Loop 3 Filter
  for (let fruit of fruits) {
    if (fruit.includes("no Mi")) {
      output += "Devil Fruit: " + fruit + "\n";
    }
  }

  output += "----------------\n";

  // Loop 4 While
  let index = 0;
  while (index < fruits.length && !fruits[index].includes("Gomu")) {
    output += "While Loop Fruit: " + fruits[index] + "\n";
    index++;
  }

  output += "----------------\n";

  // Loop 5 Do-While
  let count = 0;
  do {
    output += "Do-While Fruit: " + fruits[count] + "\n";
    count++;
  } while (count < fruits.length);

  document.getElementById("outputBox").textContent = output;
}