---
weight: 2
title: Ultimate Tic Tac Toe
---

<style>
figure {
  border: 1px #cccccc solid;
  padding: 4px;
  margin: auto;
}

figcaption {
  background-color: grey;
  color: white;
  font-style: italic;
  padding: 2px;
  text-align: center;
}
</style>

# Ultimate-Tic-Tac-Toe

Ultimate-Tic-Tac-Toe was a project I did early on in my computer science career after completing an intro into programming course at university. I used this project as a means to learn various different tools and get experience writing a UI program with control from the ground up. I did some research on a "Model-View-Controller" design pattern and decided to incorporate that, used JavaFX for the front end, and for some reason I was deadset on having an executable for this program, so I used Maven to craft that. Looking back at the code now there are a lot of things I would change, but overall it's alright, given my experience at the time of writing.

## The Game

The objective of the game is to win 3 consecutive squares in a row, just like normal tic-tac-toe, the catch however is that each square of the board is itself a 3x3 tic-tac-toe board. The larger 3 x 3 tic tac toe board is referred to as the global board. The global board contains 9 local 3 x 3 tic tac toe boards. 
<img src="/~bebeal/UTTT/Boards.png" class="center">

Initially, the first player can move anywhere. Whichever square he plays at in the local board dictates where the next player is allowed to move on the global board. That is, if the first player plays at the bottom right square in a local board, the second player is limited to placing a move in the bottom right of the global board. This pattern follows. Valid local boards are highlighted to indicate where the player is allowed to move. See the following example:

Player 1 can initially move anywhere, plays at the bottom right square in a local board. Player 2 is limited to placing a move in the bottom right of the global board. 
<img src="/~bebeal/UTTT/1.png" class="center">

Player 2 plays at the top middle in the local board. Player 1 is limited to placing a move in top middle of the global board
<img src="/~bebeal/UTTT/2.png" class="center">

If the board a player gets sent to isn't valid then the player can move to any valid location.

The objective is to win 3 local boards in a row. The game ends in a tie if nobody wins the global board and there are no valid moves left.

## Model-View-Controller

<figure>
<img src="/~bebeal/UTTT/MVC.png" class="center">
<figcaption>Fig.1 - Model-View-Controller Design Pattern</figcaption>
</figure>

### Model

I overcomplicated the model the game a bit in my opinion but it's not too bad. I have two seperate representations, an `ultimateBoard` and a `globalBoard`. The ultimate board is 4D array of `Booleans` that represents an actual ultimate-tic-tac-toe board i.e. it has rows and columns for each tic-tac-toe board which has rows and columns for each of the squares. The global board variable is a 2D array of `Booleans` and is used strictly for checking the validity of the overall course of the game to prevent having to check for wins in the local board, in hindsight, a TicTacToeBoard class that stored the win state probably would've been a better option. I used type `Boolean` to simplify the design a little as it has 3 states, `null`, `True`, and `False`. Player 1 and 2 were themselves booleans and thus could convert any of the `null` squares to `True/False`.

### View

I used fxml for my view to 1. learn the basics of a new markup language, and 2. because it integrated nice with JavaFX already. I used SceneBuilder to craft the bulk of the `src/main/resources/~/View.fxml` file. Due to some deprecations/bugs in SceneBuilder I manually added some features and edits.

### Controller

The controller stores an instance of the model so that it can manipulate it and a copy of the global `GridPane` object for the view to interpret the users input. The idea is to basically do all the work involving the integration between the view and the model here.

