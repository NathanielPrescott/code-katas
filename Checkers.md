# Checkers

https://en.wikipedia.org/wiki/Draughts

This is a multi iteration kata to teach front end and back end development.  In this exercise you will be building a game that supports two players to play against one another, while being supported on the external backend system.  For manual testing purposes you can either spin up three virtual machines or set this up on a web service of your choosing.

Each iteration can be done out of order, I am just ordering them the way I will be doing them.

## Iteration 1 - Backend

This iteration covers core functionality for movement, player tracking, general rules, restful, and database use.

### Feature: Database - generating the board

#### Board

- 8x8 board (or whichever regulation size you wish)
- Odd rows will have 'movable' squares on odd columns, while even rows will have 'movable' squares on even columns (visually these are the dark squares a player moves on)
- All other squares that are not 'movable' will be non-'movable'
- Bottom three rows of 'movable' squares will be filled with light pieces, while the top three rows of 'movable' squares will be filled with dark pieces.

Hint: Data required to be stored
>! Test 1
>! Test 2



