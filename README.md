# evolve 
Evolve is a project to demonstrate/test the process of evolving programs to play a game. 

The game chosen is the children's game tic-tac-toe. 

The following loop is performed: 

A pool of players is created at random or read from a file. 

Each player has a fixed amount of energy. It cost the player one unit of energy for each instruction it uses. 

The program chooses two players at random from the pool, and picks one to play first. 
The two players are cloned copies of the ones in the pool, so that the play does not effect the original.
The program calls the first player with a special value to indicate it is first. 
The program then calls the other player with the first player's response. 
It continues in this way, alternately calling each player with the other players response, until: 

1) A player fails to respond (runs out of energy), 2) A player replies with an invalid move, or 3) A tie results.
  
In the case of 1 or 2, that player looses and is removed from the pool.
The other player wins and gets it's energy set to the sum of the initial energies of the two players. 

In the case of a tie, no change is made to the pool. 

When a player accumulates enough energy, that player spawns. An offspring clone of the original is made. 
The parent and offspring divide the energy between the two. Occasionally, the child will get a random mutation.
Spawning may be restricted by the maximum size a pool is allowed to be. 


The program can be started from a previously stored pool of players. If not 

There are of course, a number of parameters that control these processes. 

1) The number of games to be played
2) The maximum size of the pool
3) The frequencey of mutations. 
4) The frequency of saving the pools to a file. 
5) The file name prefix. File saves as <prefix>.<date>.<time>

