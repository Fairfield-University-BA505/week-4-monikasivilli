# The HealthStats Project

## Overview
This project is designed to provide Just-in-Time practice with Python, Jupyter, and GitHub. Each class period you will complete a short assignment that applies what you have learned in the classroom that week. __Do not do assignments until they are assigned. They may change at any time until they are formally assigned.__

__You are encouraged to collaborate with your peers.__ However, you are also responsible for learning the key lessons of each assignment. So, if you need help, ask for it and pay attention to the answers. If you know how to help someone (without doing the work for them), then please help them out.

# Part 1: Lists & Control Flow
## Theory: You should know ...
* How to find and use [Markdown syntax](https://guides.github.com/features/mastering-markdown) for headlines, lists, links, etc.
* Rudimentary Python syntax, data types, and flow of control

## Practice: You be able to ...
* Write and render basic Markdown text
* Step through embedded Python code snippets
* Import data from an external file
* Perform calculations using the imported data

## Instructions
1. __Take a few minutes to read about the [Waist to Hip Ratio](https://en.wikipedia.org/wiki/Waist%E2%80%93hip_ratio).__ You should understand it well enough to explain it to your parents and walk them through doing the analysis on themselves.
2. __Open the file `w2h_data.csv` and study the data in it, which is organized as a table in *comma separated value* (or CSV) format.__ A CSV file has data in rows and columns. Each line has the same columns in the same order, with each column separated from the next by a comma.  The first line has the column names. The second line has the first row of data, with the next row below it, etc. __We are going to use Jupyter to write a short report on Waist to Hip Ratios using examples from the `w2h_data.csv` file__.  
3. __Launch Jupyter from JuoyterHub and open the file `HealthStatsPart1.ipynb` from within this repository.__ All the notebook cells are already provided, with comments used to provide instructions. Try to read through the code and make sense of what each section of the notebook is about.
4. __Edit the Markdown cells with "EDIT THIS MARKDOWN CELL".__ Instructions are given in the comments.  
  a. For the first markdown cell
5. __Read through the code in each cell, looking for "FIX THIS" comments indicating where you need to correct the code.__ For each, write the correct code, first making sure you understand what is required.
6. __Check your work by comparing with your peers.__ Just take care that your classmates may have also gotten the code wrong.
7. __Study the code again,looking for gems and dogpiles.__ You will be asked about these in the discussion questions.
8. __From the `Kernel` menu, use `Restart and Run All` to test your notebook.__ Fix any obvious errors and repeat until you think it is right. Save your notebook when you are done.
9. __Commit and sync your work to GitHub.__ Ask if you need help.
10. __Discussion Questions__
  * How long did it take you to figure out how to do a bullet list in Markdown? What other formatting tricks did you try?
  I figured out how to do the create a bullet list from looking back on past lectures. This was a helpful way to also see other formating tricks, such as, creating headers and writing in italics. I also uploaded photos from wikipedia and created a chart to display the w2h_data.csv because we were showed how to in class. 
  * Was there any code that you thought was particularly elegant? How about cryptic or buggy?
  I think this line "raw_rows = [r.rstrip('\n').split(',') for r in raw_lines]" was very elegant and I still don't fully understand how it works. I also really enjoy the code to add another column to the chart with the body shapes.
  * What does the code `raw_lines = list(f)` in the first code cell do exactly? Where can we learn more about loading files? Why do we bother closing the file at the end of the cell?
  f is defined as a variable that opens the csv file with all the data. `raw_lines = list(f)` creates a new variable that converts the information from the csv file into a list of strings which allows us to read the information and use it in python when writing code and calculating formulas. Firstly, closing the file in the end allows for the program to runs faster; if it stayed open it can use more space and slow down the performance of the program. Also, we wanted to make edits to the file, meaning adding the extra column with body-shape, therefore, we needed to close the file to make edits. 
  * In the second code cell, why do we try to clean up the data all at once? Why not just deal with it as raw strings?
  
  * What is going on in the line below, also from the second code cell?  
  ```raw_rows = [r.rstrip('\n').split(',') for r in raw_lines]```
  As I mentioned earlier I'm not 100% sure what this does, but I think it converts everything in the row from a string to a list in order to be able to iterate over the list and create conditionals for comparison and calculations. 
  * What does this do?  
  ```for raw_row in raw_rows[1:]:```
  This makes sure the iteration happens starting at the second row in the chart, not the title line. [1:] is used to tell the code to start at ID 1. 
  * In the third code cell, a list is extended by another list. What does that mean and how is that different from appending list items to the list? 
  Append only adds a single element, however, extend expands the initial list and adds the new elements at the end of the first list. The code appends an item to the list. 
 * How could we do the same thing using `append()`?
  * When might the calculation
  ```w2h_ratio = row[1]/row[2]``` give inaccurate results?
