# Algorithm notes

We implement the algorithm described [for the ADXL367](https://www.analog.com/en/resources/app-notes/an-2554.html), a 3-axis digital accelerometer. The Playdate also has a 3 axis accelerometer so this ends up working pretty well.

# Summary
- Sum of the absolute values of acceleration in three axes.
- Average the sum with the 3 previous samples.
- Store the average in an array of samples (called the window)
- if the value in the center of the window is the highest, this might be a step.
- If this might be a step and the value in the center of the window is the lowest, then it is a step.
- if it is a step, increase the step counter.
