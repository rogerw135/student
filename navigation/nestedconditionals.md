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
<h2>Nested Conditionals</h2>Deliver

<div style="
  border: 2px solid #00ffcc;
  padding: 15px;
  width: 450px;
  background-color: #0d0d0d;
  color: #00ffcc;
  font-family: monospace;
">
  <strong>Output:</strong>
  <div id="result"></div>
</div>

<script>
for (let num = 1; num <= 50; num++) {
  if (num % 1 === 0) { // factor 1
    if (num % 2 === 0) { // factor 2
      if (num % 5 === 0) { // factor 5
        if (num % 10 === 0) { // factor 10
          if (num % 25 === 0) { // factor 25
            if (num % 50 === 0) { // factor 50
              document.getElementById("result").innerHTML +=
                num + " is divisible by all factors of 50<br>";
            }
          }
        }
      }
    }
  }
}
</script>