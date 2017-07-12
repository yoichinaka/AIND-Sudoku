# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: *Student should provide answer here*

Naked twin is a pair of boxes that have same 2 numbers (= 2 length).
If there is naked twins in a units, it means we can remove the naked twin numbers
from other boxes, because 2 numbers in naked twin are must be only these boxes,
althogh we cannot indentify the exact box locaion,
but we can remove these 2 numbers from other boxes.
Then we can search naked twin for other unit and repeat this for all units.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: *Student should provide answer here*

I made diag and diag1 for diagonal units and add these two as diag_unit_list.
And then add to unitlist that is the list of the all units.
daig and diag1 are,
[A1, B2, C3, D4, E5, F6, G7, H8, I9] and [A9, B8, C7, D6, E5, F4, G3, H2, I1].
Diagonal unit has the same rule as other units. 
This means only one number can be used in diagnol unit.
I utilize the same 'eliminate' function to remove the only one value from 
diagonal units.

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solution.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Submission
Before submitting your solution to a reviewer, you are required to submit your project to Udacity's Project Assistant, which will provide some initial feedback.  

The setup is simple.  If you have not installed the client tool already, then you may do so with the command `pip install udacity-pa`.  

To submit your code to the project assistant, run `udacity submit` from within the top-level directory of this project.  You will be prompted for a username and password.  If you login using google or facebook, visit [this link](https://project-assistant.udacity.com/auth_tokens/jwt_login for alternate login instructions.

This process will create a zipfile in your top-level directory named sudoku-<id>.zip.  This is the file that you should submit to the Udacity reviews system.

