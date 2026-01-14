---
layout: page
title: Boolean Lesson
permalink: /booleanlesson/
comments: true
---

A boolean value can be **true** or **false**. Toggle the boxes to see how it works!

```javascript
let isHomeworkDone = true;
let isTired = false;
// ...
if (isHomeworkDone) {
  console.log("You can relax!");
} else {
  console.log("Finish your homework!");
}

if (isTired) {
  console.log("Go take a nap.");
} else {
  console.log("Keep going!");
}


A boolean value can be **true** or **false**. Toggle the boxes to see how it works!

<label>
  <input type="checkbox" id="homeworkCheckbox">
  Is Homework Done?
</label>

<br><br>

<label>
  <input type="checkbox" id="tiredCheckbox">
  Are you Tired?
</label>

<div id="boolean-box" style="
    margin-top: 20px;
    padding: 20px;
    border-radius: 10px;
    width: 350px;
    text-align: center;
    font-weight: bold;
    font-size: 1.2em;
    color: white;
">
  Your status will appear here.
</div>

<script>
  const homeworkCheckbox = document.getElementById('homeworkCheckbox');
  const tiredCheckbox = document.getElementById('tiredCheckbox');
  const box = document.getElementById('boolean-box');

  function updateBox() {
    const isHomeworkDone = homeworkCheckbox.checked;
    const isTired = tiredCheckbox.checked;

    let messages = [];

    // Messages
    messages.push(isHomeworkDone ? "You can relax! ✅" : "Finish your homework! ❌");
    messages.push(isTired ? "Go take a nap! 😴" : "Keep going! 💪");

    box.textContent = messages.join(" | ");

    // Color logic
    if (isHomeworkDone && !isTired) {
      box.style.backgroundColor = "#28a745"; // green
    } else if (!isHomeworkDone && isTired) {
      box.style.backgroundColor = "#dc3545"; // red
    } else {
      box.style.backgroundColor = "#ffc107"; // yellow
      box.style.color = "black"; // better contrast on yellow
    }

    // Reset text color for green/red
    if (isHomeworkDone && !isTired || !isHomeworkDone && isTired) {
      box.style.color = "white";
    }
  }

  homeworkCheckbox.addEventListener('change', updateBox);
  tiredCheckbox.addEventListener('change', updateBox);
</script>
