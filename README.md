# SAT-Solver-for-Tiling-Dominoes
A SAT solver that outputs DIMACS format SAT encodings without using MiniSat or Satispy.

This was done as a final project for my Theory of Computation Class, and seeks to answer the question: Given a rectangular grid with some of the squares blocked off, can the remaining squares be covered with non-overlapping dominos? 

# Example
Input will be a string in the format of: Width,Height,(XCoord1,YCoord1),(XCoord2,YCoord2)
(XCoord1,YCoord1) marks the first square we want to block.
(XCoord2,YCoord2) marks the second square we want to block off.
... and so for for blocking off

Note: it is NOT necessary to include any blocked off squares. If you do not wish to have any squares blocked off, simply type in the format: Width, Height

3,5,(1,1),(1,5),(2,4)

![Example Grid](Images/blank-grid.png)


Output will be a printed out string of the DIMACS format SAT encodings:



# Special Thanks
@msoos for his incredible online SAT solver, which can be found here: https://msoos.github.io/cryptominisat_web/
