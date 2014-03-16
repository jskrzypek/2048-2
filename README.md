# 2048²

I modified code I found here: http://www.csie.ntu.edu.tw/~b01902112/9007199254740992/ to provide more random tiles on each move, and increase the possible added total added per move to make the goal more achievable. Adding 4 to the board per move, and assuming one move takes 200 ms, you're looking at more than 14 million years to beat the game. 

Here tile values are normally distributed, such that the log-base 2 of the tile's value determines its sigma-level of occuring, i.e. ~68% percent of the tiles will be 2, ~27% will be 4, ~4% will be 8, etc. with 0.001% of all tiles having a value of 32, the maximum value of a new tile. 

Additionally, up to 4 new tiles are added to the board, and again, the normal distribution is followed such that 13.16% of moves result in 1 new tile, another 13.16% result in 4, and the rest of the distribution is split between 2 or 3 new tiles. Thus, 68% of moves will reult in either 2 or 3 tiles.

The new maximum value added to the board is thus 32 on each of 4 tiles, or 128, though there's less than 1.5e-15% chance of that happening.
