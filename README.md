# comcom_projects

The Blocks puzzle in this project has numerous variations available on the web and in mobile apps (for example, you can play an online Blocks Puzzle). You are presented with a grid of square cells (initially empty) and a set of some number of pieces formed from configurations of square, cell-sized blocks (we'll call these pieces the hand), which you try to arrange in order to cover empty cells of the grid. After each piece is placed, any rows and columns of the grid that have become completely filled are cleared. After you place all the pieces in the hand, it is refilled with the same number of pieces as before. Play continues until none of the pieces in the hand can fit anywhere on the board.

For example, consider the board on the left below. The middle piece of the hand (shown below the board) may be placed at either of the places indicated by the pink-shaded areas. If we choose to place its reference point on the square (1,0) (row 1, column 0), we get the middle board. (The reference point of a piece refers to the upper left corner of the smallest rectangle that contains the piece. Depending on the shape of the piece, it may or may not actually be filled. For example, the first (middle) piece we placed had its reference point filled; the second (leftmost) piece did not.) If we then place the leftmost piece at the pink-shaded position on that board (so that its reference point is at row 2, column 5), we will fill all of row 2, which will then be cleared to yield the board on the right.

Sample Boards and Moves

By default, the board consists of 64 cells in an 8x8 grid, and the hand contains three pieces at a time. Your program will be able to change these parameters to make boards and hands of varying sizes.

Scoring:

One point for each cell that gets filled by a piece
One point for each cell that then gets cleared
Bonus for clearing at least one row or column.
The bonus is the total number of cells in all cleared rows, plus the total number of cells in all cleared columns, then multiplied by the number of consecutive moves in which at least one line or column was cleared.
When using the GUI (Graphical User Interface), scores appear above the board, as shown below.

Scoring Examples

For example, assume that in the board at the left above, the previous move added a piece without clearing any squares. Inserting the rightmost piece in the hand at the position indicated by the pink shading yields the middle board. The piece added contained 4 cells and caused the clearing of one row and one column, which cleared 15 cells (the cell at (0,2) is counted only once). Since row 0 and column 2 were cleared (both with 8 cells), we get a bonus of 16 (this time, square (0, 2) is counted twice). Since we assume that the previous move did not result in clearing, the number of consecutive moves in which a row or column is cleared is 1 at this point, so that placing this piece results in a score of 4+15+1×16=35, and the score for the round increases to 185. Now we add the indicated piece to the middle board at the pink-shaded position. This adds 3 cells and then clears 8 (one row). Since with this move, the number of consecutive moves that clear a row or column is 2, this leads to an additional 3+8+2×8=27 points, bringing the total for the round to 212.
