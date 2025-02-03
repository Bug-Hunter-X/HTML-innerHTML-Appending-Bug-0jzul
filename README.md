# Uncommon HTML Bug: innerHTML Appending Issue

This repository demonstrates an uncommon bug related to using `innerHTML` in JavaScript to append content to an existing HTML element.  The issue arises from how `innerHTML` handles existing content when a new string is assigned.

## Bug Description

The bug involves appending new HTML content to an element using `innerHTML`. When the new content is simply added to the end using the `+` operator, the existing content is duplicated, leading to unintended visual results. This behavior is not immediately obvious and can be tricky to debug.

## How to Reproduce

1. Open `bug.html` in a web browser.
2. Observe the content of the `div` with the id `myDiv`.
3. The text should initially read: "This text is initially visible."
4. The Javascript appends new text to the div using innerHTML, but incorrectly duplicates the initial content.

## Solution

The solution involves using DOM manipulation methods like `insertAdjacentHTML` to correctly add the content. This avoids unexpected behaviour related to re-assigning innerHTML.

Check `bugSolution.html` for a corrected version that demonstrates this approach.
