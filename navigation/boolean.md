---
layout: page
title: Boolean
permalink: /boolean/
comments: true
---

---
layout: page
title: Boolean
permalink: /boolean/
comments: true
---

<label>
  <input type="checkbox" id="check">
  Test number (checked = 7, unchecked = 8)
</label>

<p id="result"></p>

<script>
function isPositiveAndOdd(num) {
  let isPositive = num > 0;
  let isOdd = num % 2 !== 0;
  return isPositive && isOdd;
}

const checkbox = document.getElementById("check");
const result = document.getElementById("result");

function updateResult() {
  const num = checkbox.checked ? 7 : 8;
  result.textContent = "Result: " + isPositiveAndOdd(num);
}

// run once + whenever checkbox changes
updateResult();
checkbox.addEventListener("change", updateResult);
</script>