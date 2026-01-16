---
layout: page
title: Nested Conditionals
permalink: /nestedconditionals/
comments: true
---
for (let num = 1; num <= 50; num++) {
  if (num % 1 === 0) { // factor 1
    if (num % 2 === 0) { // factor 2
      if (num % 5 === 0) { // factor 5
        if (num % 10 === 0) { // factor 10
          if (num % 25 === 0) { // factor 25
            if (num % 50 === 0) { // factor 50
              console.log(num + " is divisible by all factors of 50");
            }
          }
        }
      }
    }
  }
}
<div style="border: 2px solid #4caf50; padding: 15px; width: 400px; background-color: #111; color: #4caf50; font-family: monospace;">
  <strong>Numbers divisible by all factors of 50:</strong>
  <ul id="output"></ul>
</div>

<script>
for (let num = 1; num <= 50; num++) {
  if (num % 1 === 0) {
    if (num % 2 === 0) {
      if (num % 5 === 0) {
        if (num % 10 === 0) {
          if (num % 25 === 0) {
            if (num % 50 === 0) {
              const li = document.createElement("li");
              li.textContent = num + " is divisible by all factors of 50";
              document.getElementById("output").appendChild(li);
            }
          }
        }
      }
    }
  }
}
</script>