# Bluffing-Game
Bluffing Game ML Project
v0.0
This code plays the following Poker like bluffing game and evolves strategies using reinforcement learning. I am doing this to practice Python code and to experiment with ML methods.
The game works as follows. Two players, A and B, each bets  1.TheyareeachgivenarandomcardfromadeckD(asetofnumbersinitiallydiscrete,maychangetocontinuous).PlayerAcanthendecidetopass,inwhichcasethehighercardgetsthe
 2, or raise, adding another dollar to the pot. If A raises, B chooses to fold, in which case A gets the pot, or call, in which case the holder of the highest card gets the $4 pot. If they are equal, they split. Thus the payouts are as follows.
A Choice	B Choice	Higher Card	Payout to A	Payout to B
Pass	N/A	A	+1	-1
Pass	N/A	B	-1	+1
Pass	N/A	Ti	0	0
Raise	Fold	N/A	+1	-1
Raise	Call	A	+2	-2
Raise	Call	B	-2	+2
Raise	Call	Tie	0	0
----------	----------	-------------	-------------	------------
Idea is from https://fivethirtyeight.com/features/dont-throw-out-that-calendar/ where the game is analyzed for the set {1,2,3,4,5,6}. There is an optimum mixed strategy for A involving bluffing, and multiple optimum strategies -- all mixed -- for B. I want to see if, and how fast, ML can find these strategies.
