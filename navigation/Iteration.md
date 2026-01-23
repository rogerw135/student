---
layout: page
title: Iteration
permalink: /iterations/
comments: true
---
let fruits = ["Heart Shaped Herb", "Yami Yami no Mi", "Gomu Gomu no Mi"];

// -------------------------
// Loop 1: Forward (basic counting loop)
// Condition: i increases while less than array length
// -------------------------
for (let i = 0; i < fruits.length; i++) {
    console.log("Forward:", fruits[i]);
}

console.log("------------------");

// -------------------------
// Loop 2: Backward
// Condition: i decreases while >= 0
// -------------------------
for (let i = fruits.length - 1; i >= 0; i--) {
    console.log("Backward:", fruits[i]);
}

console.log("------------------");

// -------------------------
// Loop 3: for...of with IF condition
// Condition inside loop filters results
// -------------------------
for (let fruit of fruits) {
    if (fruit.includes("no Mi")) {   // only Devil Fruits
        console.log("Devil Fruit:", fruit);
    }
}

console.log("------------------");

// -------------------------
// Loop 4: while loop
// Condition: runs until a name contains "Gomu"
// -------------------------
let index = 0;
while (index < fruits.length && !fruits[index].includes("Gomu")) {
    console.log("While Loop Fruit:", fruits[index]);
    index++;
}

console.log("------------------");

// -------------------------
// Loop 5: do...while loop
// Condition checked AFTER first run
// -------------------------
let count = 0;
do {
    console.log("Do-While Fruit:", fruits[count]);
    count++;
} while (count < fruits.length);