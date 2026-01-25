---
layout: page
title: Iteration
permalink: /iterations/
comments: true
---
function runLoops() {
  const fruits = ["Heart Shaped Herb", "Yami Yami no Mi", "Gomu Gomu no Mi"];
  let output = "";

  // Loop 1: Forward
  for (let i = 0; i < fruits.length; i++) {
    output += "Forward: " + fruits[i] + "\n";
  }

  output += "----------------\n";

  // Loop 2: Backward
  for (let i = fruits.length - 1; i >= 0; i--) {
    output += "Backward: " + fruits[i] + "\n";
  }

  output += "----------------\n";

  // Loop 3: for...of with condition
  for (const fruit of fruits) {
    if (fruit.includes("no Mi")) {
      output += "Devil Fruit: " + fruit + "\n";
    }
  }

  output += "----------------\n";

  // Loop 4: while
  let index = 0;
  while (index < fruits.length && !fruits[index].includes("Gomu")) {
    output += "While Loop Fruit: " + fruits[index] + "\n";
    index++;
  }

  output += "----------------\n";

  // Loop 5: do...while
  let count = 0;
  do {
    output += "Do-While Fruit: " + fruits[count] + "\n";
    count++;
  } while (count < fruits.length);

  document.getElementById("outputBox").textContent = output;
}

function clearBox() {
  document.getElementById("outputBox").textContent = "";
}
}