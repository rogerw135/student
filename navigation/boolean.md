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
  <input type="checkbox" id="testCheck">
  Check this box to test the number 7 (unchecked = test 8)
</label>

<p id="output"></p>

<script>
function isPositiveAndOdd(num) {
  let isPositive = num > 0;
  let isOdd = num % 2 !== 0;
  return isPositive && isOdd;
}

document.getElementById("testCheck").addEventListener("change", function () {
  let num = this.checked ? 7 : 8;
  document.getElementById("output").textContent =
    "Number: " + num + " → " + isPositiveAndOdd(num);
});
</script>