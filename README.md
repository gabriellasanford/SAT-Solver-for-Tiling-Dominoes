# SAT-Solver-for-Tiling-Dominoes
A SAT solver that outputs DIMACS format SAT encodings without using MiniSat or Satispy.

This was done as a final project for my Theory of Computation Class, and seeks to answer the question: Given a rectangular grid with some of the squares blocked off, can the remaining squares be covered with non-overlapping dominos? 

## Explanation
Input will be a string in the format of: Width,Height,(XCoord1,YCoord1),(XCoord2,YCoord2)
(XCoord1,YCoord1) marks the first square we want to block.
(XCoord2,YCoord2) marks the second square we want to block off.
... and so for for blocking off

Note: it is NOT necessary to include any blocked off squares. If you do not wish to have any squares blocked off, simply type in the format: Width, Height

## Example
Input: 3,5,(1,1),(1,5),(2,4)

![Example Grid](Images/blank-grid.png)


Output will be a printed out string of the DIMACS format SAT encodings:

![Python Program Output Sample](https://github.com/gabriellasanford/SAT-Solver-for-Tiling-Dominoes/blob/master/Images/gif.gif)

In order to determine if a solution is SATisfiable, I then take the output that was printed out from the python program and input it into an online SAT solver:

![DIMACS SAT SOLVER](https://github.com/gabriellasanford/SAT-Solver-for-Tiling-Dominoes/blob/master/Images/satsolver.gif)
 
The top right corner will read UNSAT (as in the example) if the problem is unsatisfiable for the given input, and will return SAT if it is satisfiable and will also return the clauses found to be true and false at the bottom of the screen.

# Special Thanks
@msoos for his incredible online SAT solver, which can be found here: https://msoos.github.io/cryptominisat_web/
