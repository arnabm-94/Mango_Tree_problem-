# Mango_Tree_problem-
There is a farm organized as an N*N grid. Each square in the grid either has or does not have a mango tree. The farm has to divided among 4 people by drawing one horizontal line and  one vertical line to divide the field into 4 rectangles.  Three people will choose three of the four rectangles and the last person will get the last one. 
==========================================================================================================================================================================================================\


To solve this problem, we need to find a way to divide the grid into four rectangles 
by drawing one horizontal and one vertical line such that the number of mango trees 
in the rectangle with the fewest trees is maximized. 
This ensures the most balanced distribution of mango trees among the four people.
-------------------------------------------------------------------------------



#Prefix Sum Matrix: We create a prefix sum matrix to efficiently compute the sum of elements 
in any subrectangle of the grid. The prefix sum at position (i, j) represents the sum of all 
elements in the subrectangle from (0, 0) to (i-1, j-1).

#Populate Prefix Sum Matrix: The prefix sum for each cell is calculated using the values above, 
to the left, and diagonally above-left from the current cell in the grid.

#Dividing the Grid: We iterate over all possible positions for the horizontal and 
vertical lines that can divide the grid. For each position (i, j) of the lines, 
we calculate the number of mango trees in each of the four resulting rectangles using the prefix sum matrix.

#Finding the Minimum Trees in a Section: For each division, we determine the minimum number of trees among 
the four sections. We keep track of the maximum value of these minimum counts, ensuring the most balanced 
distribution.
