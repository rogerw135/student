---
layout: page
title: Boolean
permalink: /boolean/
comments: true
---
// Step 1: Create an array with 5 items
let favoriteMovies = ["Inception", "The Matrix", "Spirited Away", "Interstellar", "The Dark Knight"];

// Step 2: Print the entire array
console.log("Entire array:", favoriteMovies);

// Step 3: Access and print the first element (index 0)
console.log("First element:", favoriteMovies[0]);

// Step 4: Access and print the last element
console.log("Last element:", favoriteMovies[favoriteMovies.length - 1]);

// Step 5: Print the total number of items in the array
console.log("Total number of items:", favoriteMovies.length);
Entire array: [
  'Inception',
  'The Matrix',
  'Spirited Away',
  'Interstellar',
  'The Dark Knight'
]
First element: Inception
Last element: The Dark Knight
Total number of items: 5
// Step 1: Start with the shopping list
let shoppingList = ["milk", "eggs", "bread", "cheese"];

// Print the original array
console.log("Original array:", shoppingList);

// Step 2: Change the second item (index 1) to "butter"
shoppingList[1] = "butter";

// Step 3: Add "yogurt" to the end using push()
shoppingList.push("yogurt");

// Step 4: Remove "bread" from the array
// First, find the index of "bread"
let breadIndex = shoppingList.indexOf("bread");
if (breadIndex !== -1) {
  shoppingList.splice(breadIndex, 1); // remove 1 item at that index
}

// Step 5: Print the final array
console.log("Final array:", shoppingList);
Original array: [ 'milk', 'eggs', 'bread', 'cheese' ]
Final array: [ 'milk', 'butter', 'cheese', 'yogurt' ]