---
layout: page
title: Nested Conditionals
permalink: /nestedconditions/
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
