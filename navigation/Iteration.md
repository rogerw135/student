---
layout: page
title: Iteration
permalink: /iterations/
comments: true
---
function runLoops() {
  const fruits = ["Heart Shaped Herb", "Yami Yami no Mi", "Gomu Gomu no Mi"];
  let output = "";

  for (let i = 0; i < fruits.length; i++) {
    output += "Forward: " + fruits[i] + "\n";
  }

  output += "----------------\n";

  for (let i = fruits.length - 1; i >= 0; i--) {
    output += "Backward: " + fruits[i] + "\n";
  }

  output += "----------------\n";

  for (const fruit of fruits) {
    if (fruit.includes("no Mi")) {
      output += "Devil Fruit: " + fruit + "\n";
    }
  }

  output += "----------------\n";

  let index = 0;
  while (index < fruits.length && !fruits[index].includes("Gomu")) {
    output += "While Loop Fruit: " + fruits[index] + "\n";
    index++;
  }

  output += "----------------\n";

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
<!DOCTYPE html>
<html>
<head>
  <title>Loop Output with Checkboxes</title>
  <style>
    body { font-family: Arial, sans-serif; padding: 20px; background: #f9f9f9; }
    h2 { margin-bottom: 10px; }
    #counter { margin-bottom: 20px; font-weight: bold; }
    .loop-section { margin-bottom: 20px; padding: 10px; border-radius: 8px; }
    .forward { background-color: #d0f0c0; }      /* light green */
    .backward { background-color: #f0d0c0; }     /* light red */
    .devil { background-color: #d0d0f0; }        /* light blue */
    .while { background-color: #f0f0c0; }        /* light yellow */
    .do-while { background-color: #f0d0f0; }     /* light purple */
    label { margin-left: 6px; }
    button { margin-right: 10px; margin-top: 10px; padding: 6px 12px; }
  </style>
</head>
<body>

<h2>Loop Output with Checkboxes</h2>
<div id="counter">Checked: 0</div>
<div id="outputBox"></div>

<button onclick="runLoops()">Run Loops</button>
<button onclick="clearBox()">Clear</button>

<script>
const outputBox = document.getElementById("outputBox");
const counter = document.getElementById("counter");

function updateCounter() {
  const checkedBoxes = outputBox.querySelectorAll("input[type='checkbox']:checked");
  counter.textContent = `Checked: ${checkedBoxes.length}`;
}

function createCheckbox(labelText, parent) {
  const div = document.createElement("div");
  const checkbox = document.createElement("input");
  checkbox.type = "checkbox";
  checkbox.addEventListener("change", updateCounter);
  const label = document.createElement("label");
  label.textContent = labelText;
  div.appendChild(checkbox);
  div.appendChild(label);
  parent.appendChild(div);
}

function runLoops() {
  const fruits = ["Heart Shaped Herb", "Yami Yami no Mi", "Gomu Gomu no Mi"];
  outputBox.innerHTML = ""; // Clear previous output
  counter.textContent = "Checked: 0";

  // 1️⃣ Forward loop
  const forwardSection = document.createElement("div");
  forwardSection.className = "loop-section forward";
  forwardSection.innerHTML = "<strong>Forward Loop:</strong>";
  outputBox.appendChild(forwardSection);
  for (let i = 0; i < fruits.length; i++) {
    createCheckbox("Forward: " + fruits[i], forwardSection);
  }

  // 2️⃣ Backward loop
  const backwardSection = document.createElement("div");
  backwardSection.className = "loop-section backward";
  backwardSection.innerHTML = "<strong>Backward Loop:</strong>";
  outputBox.appendChild(backwardSection);
  for (let i = fruits.length - 1; i >= 0; i--) {
    createCheckbox("Backward: " + fruits[i], backwardSection);
  }

  // 3️⃣ Devil Fruits (for-of with condition)
  const devilSection = document.createElement("div");
  devilSection.className = "loop-section devil";
  devilSection.innerHTML = "<strong>Devil Fruits (contains 'no Mi'):</strong>";
  outputBox.appendChild(devilSection);
  for (const fruit of fruits) {
    if (fruit.includes("no Mi")) {
      createCheckbox("Devil Fruit: " + fruit, devilSection);
    }
  }

  // 4️⃣ While loop
  const whileSection = document.createElement("div");
  whileSection.className = "loop-section while";
  whileSection.innerHTML = "<strong>While Loop (stops at 'Gomu'):</strong>";
  outputBox.appendChild(whileSection);
  let index = 0;
  while (index < fruits.length && !fruits[index].includes("Gomu")) {
    createCheckbox("While Loop Fruit: " + fruits[index], whileSection);
    index++;
  }

  // 5️⃣ Do-while loop
  const doWhileSection = document.createElement("div");
  doWhileSection.className = "loop-section do-while";
  doWhileSection.innerHTML = "<strong>Do-While Loop:</strong>";
  outputBox.appendChild(doWhileSection);
  let count = 0;
  do {
    createCheckbox("Do-While Fruit: " + fruits[count], doWhileSection);
    count++;
  } while (count < fruits.length);
}

function clearBox() {
  outputBox.innerHTML = "";
  counter.textContent = "Checked: 0";
}
</script>

</body>
</html>

