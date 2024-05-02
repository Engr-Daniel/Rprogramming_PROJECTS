Use R to make art and create imaginary flowers inspired by nature.

Instructor:
Antonio Sánchez Chinchón
Data Scientist at Telefónica


Project Description
R is a tool for doing serious statistics and data analysis. But not everything in life can be serious, life is also beautiful, and R can make beautiful things too. R can make art.

The arrangement of leaves on a plant stem is ruled by spirals. This fact is called phyllotaxis and it is a nice example of how mathematics can describe patterns in nature. In this project, we will invent flowers using this fact.

This R project assumes you have familiarity with the ggplot2 package. If you want to see more examples of how you can use R to make art, you should check out the Fronkonstin blog created by Antonio Sánchez Chinchón.



Task 1: Instructions
Load the package.

Read the project introduction.
Load the ggplot2 package.


Task 2: Instructions
Create a scatter plot of 50 points arranged in a circle.

Read through the given code to create the data frame, df.
Complete the statement to make a scatter plot using geom_point().


Task 3: Instructions
Create a scatter plot of spiralzed points.

Create the variable points which defines the number of points to draw and set its value to 500.
Create another variable called angle and set its value to π(3 − √5) .
Make a scatter plot.


Task 4: Instructions
Remove plot components and change the background color.

Remove the grid, ticks, axes titles, and axes text from the spiral plot, and make the background white.

Task 5: Instructions
Make the plot more aesthetically appealing.

Copy and paste the last lines of code that created the plot from Task 4.
Change the call to geom_point() so that the size of points equals 8, the alpha (transparency) equals 0.5, and the color is darkgreen.
After doing this, you should see a plot where all points will have the same size, alpha, and color. The alpha parameter will produce a darker color where points overlap.

Task 6: Instructions
Create a plot that looks like a dandelion.

Copy and paste the solution from Task 5.
Within geom_point(), map the size aesthetic to the variable t, remove the color, and set the shape (outside the aesthetics) to an asterisk (*).
Remove the legend from the plot.


Task 7: Instructions
Create a sunflower plot.

Copy and paste the solution from Task 6.
Change the shape of all points to filled triangles, and change the color of the points to yellow.
Change the color of the background to "darkmagenta".


Task 8: Instructions
Change the value of the angle.

Change the value of angle from the Golden Angle (which is about 2.4) to 2.0 .
Copy and paste the code from Task 7 and create the plot.

Task 9: Instructions
Create a magenta flower by changing a few plot parameters.

Set angle to 13*pi/180, and double the amount of points.
Within geom_point(), set alpha to 0.1, shape to open circles, and color to "magenta4". Also, remove size from the aesthetics and set it to 80.
Set the background fill to "white".












