---
layout: lesson
title: "10: Loop Structures"
---
### Loops

Continuing our survey of utilitarian structures in JavaScript we turn to discuss how we create repeating blocks of code.

***Read Duckett, Chapter 4, pp.170-182.***

This is another short section of reading but it packs a big power punch for processing. However, jQuery also builds on this for some of our most common use cases. Very often we want to repeat an operation for each item we selected using jQuery. Thankfully we have another shortcut for such common operations.

***Read Duckett, Chapter 7, pp.324-325.***

To debrief, note the following:

1. Loops must have an "exit clause" so that they don't run on forever and ever.
2. The **most basic** of such clauses is a counter that changes on each iteration (like in a `for` loop). IN such a case, the loop is set up to repeat as long as that counter is within a certain range.
3. The **most common** of such clauses is to continue an operation *for each* item in a list. As long as we have items left in the list we'll continue the loop. When we reach the end, the loop stops repeating.
4. More complex loops are useful but take extra thought. Just keep in mind:
    1. A loop must have a condition that will *eventually* change and cause the loop to stop.
    2. Therefore, the declaration block must include a logical possibility for this condition to change.

#### Study Questions

1. What are loops in programming languages like JavaScript and what do they enable us to do?
2. **SKILL:** Create vanilla JavaScript loops using `for`, `while`, and `do... while`.
3. **SKILL:** Loop through a jQuery result set using `.each()`.
