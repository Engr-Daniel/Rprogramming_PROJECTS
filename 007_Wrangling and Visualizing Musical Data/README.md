# WRANGLING AND VISUALIZING MUSICAL DATA

Wrangle and visualize musical data to find common chords and compare the styles of different artists.

## Project Description
Apply data-wrangling and visualization tools from the tidyverse to musical data. Find the most common chords and chord progressions in a sample of pop/rock music from the 1950s-1990s, and compare the styles of different artists.

This project assumes familiarity with standard TidyVerse tools for R, in particular the tibble data structure and the dplyr and ggplot2 packages. No specific musical knowledge is required, though it may give you ideas for further exploration of the dataset after completing the project.

## DATA
This project uses a parsed and cleaned version of the [McGill Billboard Dataset](http://ddmal.music.mcgill.ca/research/billboard), version 2.0 (CC0 license).


**Task 1: Read in the McGill Billboard chord dataset.**

- Load in the dplyr, readr, and ggplot2 packages.
- Read in 'datasets/bb_chords.csv' using read_csv and assign it to bb.
- Display the first rows of bb.

**Task 2: Find the most common chords in the McGill Billboard Dataset**

- Count the number of occurrences of each raw chord type in the dataset (bb) using count(), and sort the results from most common (highest count) to least common (lowest count).
- Store the result in bb_count.
- Display the 20 most common chords.

**Task 3: Plot the top 20 chords as a flipped bar plot.**

- Starting with the first 20 records from bb_count, use mutate to create a new column share with the percentage of how often each chord type occurs.
- Also using mutate, reorder the chord column according to the value in share.
- Pipe the results into ggplot() and make a column plot where the X axis represents chord and the Y axis is represents share.
- Make your plot more readable by adding labels with xlab() and ylab(), and by flipping the plot using coord_flip().

**Task 4: Create a count of chord bigrams.**

- Use mutate() to add two new columns to bb: next_chord and next_title. These should contain the data from the chord and title columns, but shifted one row up. Use the lead() function inside your mutate() command to do this.
- Create a bigram column that concatenates chord with next_chord, with a space in between.
Use filter() to remove any records in our new data frame where title and next_title are not identical.
- Count the number of occurrences of each bigram type and store the results in bb_bigram_count.
- Display the 20 most common chord bigrams.

**Task 5: Create a flipped bar plot that shows the 20 most common chord bigrams.**

- Copy your code from Step 3, and modify it to work with bb_bigram_count instead of bb_count.
- Adjust the plot labels to fit chord changes instead of just chords.


**Task 6: Find and display the 30 artists with the most songs in the McGill Billboard Dataset.**

- Using bb, isolate the artist and title columns using select().
- We still have one record per chord. Use unique() to remove duplicates and leave a single record per song.
- As in earlier tasks, use count() to find how many songs each artist has in the dataset, and sort the results in descending order.
- Display the first 30 records in the sorted table.

**Task 7: Add a new column instrument to bb, including "piano" or "guitar" for piano- and guitar-driven songs.**

- Use inner_join() with tags to attach an instrument column to bb and assign the result to bb_tagged.
- Display the new data frame bb_tagged to make sure the join was successful.

**Task 8: Created a faceted plot that shows the frequency of the most common chords side-by-side for songs by piano- and guitar-driven artists.**

- Starting with bb_tagged, use filter() to keep only the top_20 chords.
- Use count() to find the number of times each chord occurs for each instrument, and sort the results.
- Pipe the results to ggplot() and make a bar plot, using chord as the X axis and n (the result of count()) as your Y axis.
- Use facet_grid() to place guitar and piano plots side by side for comparison. Then use coord_flip() for readability, and provide appropriate labels for the X and Y axes.

**Task 9: Create the same faceted plot as in Task 8, but for chord bigrams.**

- Copy and modify your code from Task 4 to add a bigram column, this time to bb_tagged.
- Copy and modify your code from Task 8 to produce a faceted plot of bigram frequency from the top_20_bigrams that compares guitar- and piano-driven songs.
- Remember to change all references to chords (including in the axis labels) to bigrams.

**Task 10: Complete the project by confirming the validity of the hypothesis, as well as the need for further data analysis to draw a conclusion.**

- Is the hypothesis that guitar-driven and piano-driven songs have different chord tendencies valid and worth deeper exploration? TRUE or FALSE? Set hypothesis_valid to reflect your answer.
- To draw a conclusion about this hypothesis, do we still need to explore more data? TRUE or FALSE? Set more_data_needed to reflect your answer.


#### INSTRUCTOR:
Kris Shaffer

Data scientist and instructional technology specialist
