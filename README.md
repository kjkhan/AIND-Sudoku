# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver
Student:  Kahlil Khan, kahlilkhan@gmail.com

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: The naked twin strategy constrains the values of other boxes in the same unit by ensuring no other boxes in that unit share any digits with the twins.  It does this by eliminating either of the twin's values as a possiblity for the remaining unsolved boxes.  This often reduces the number of digits in these peers, increasing the efficiency of the other strategies and the recursive depth-first search method.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: By adding the two major diagonals as units to the unitlist and peers dictionaries, these units become constraints to the existing solution functions (eliminate, only choice, naked twins, reduce, and search) that rely on those dictionaries to identify peers.  For example, the "eliminate" function now factors in the diagonal units when reviewing a box's peers, and if that box falls on either of the major diagonals, there are additional peers to iterate through for possible value elimination.

### Install

This project requires Python 3.  Pygame for visualization is optional.

### Code

* `solutions.py` - Sukodu grid encoding and strategy functions (eliminate, only choice, naked twins, search)
* `solution_test.py` - Unit test cases; run `python solution_test.py`.
* `PySudoku.py` - Code for visualizing your solution.
* `visualize.py` - Code for visualizing your solution.

### Data

The data consists of a text file of diagonal sudokus.