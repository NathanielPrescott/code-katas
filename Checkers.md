# Checkers

https://en.wikipedia.org/wiki/Draughts

This is a multi iteration kata to teach front end and back end development.  In this exercise you will be building a game that supports two players to play against one another, while being supported on the external backend system.  For manual testing purposes you can either spin up three virtual machines or set this up on a web service of your choosing.

Each iteration can be done out of order, I am just ordering them the way I will be doing them.

## Iteration 1 - BackEnd

This iteration covers core functionality for movement, player tracking, general rules, restful, and database use.

### Feature: Database - board/pieces

#### Board

- 8x8 board (or whichever regulation size you wish)
- Odd rows will have 'movable' squares on odd columns, while even rows will have 'movable' squares on even columns (visually these are the dark squares a player moves on)
- All other squares that are not 'movable' will be non-'movable'
- Bottom three rows of 'movable' squares will be filled with light pieces, while the top three rows of 'movable' squares will be filled with dark pieces.

#### Players

- 2 players per game with each player getting either light or dark pieces
- Removes a players pieces when they are 'captured'

### Feature: Restful Endpoint

- Collect the current players move on their turn
- Update the players board with what the other player did

### Feature: Validation?

- Validate that a player is entering proper moves, this could technically also be done on the front end

## Iteration 2 - FrontEnd

This iteration covers the logic necessary to visually play the game.

### Feature: Consuming data from the restful endpoint

- Collect the board games state with each players pieces layout

### Feature: Displaying data from the restful endpoint

- Generate an 8x8 board
- Allocate the pieces to the board

### Feature: Player Moves

- Pieces can be moved diagonally only
- Pawns (men) can only move forward in their respective players direction
- Kings can move forward and backward
- Kings can only be created when a Pawn reaches its opponents back line (or the furthest row from the players starting side)
- To remove a piece from the board a players piece must be diagonally next to their opponents piece with an empty space diagonally from that, this can be refered to as 'hopping' (reference the wiki page to see how this works if you are confused)
- A player may string together multiple hops with the same piece as long as the above conditions are met
- When all of a players pieces are removed they will lose
- Pick a size that goes first or just randomize it

## Iteration 3 - Prettify

This iteration is for those who are really enjoying their checkers app.  You can always pick and choose which Features you want to implement!

### Feature: Look and feel

- Flesh out the board game look and feel (primarily use css to enhance the user experience)

### Feature: Multi-Game Overhaul

- Allow for multiple games to be spun up and used depending on how many users are using the application
- An additional interface could be created for this feature or you can allocated waiting users with other waiting users


Good luck!
