# Importing Modules:
    from turtle import Turtle, Screen: Imports the Turtle graphics library for creating graphics and animations.
    from paddle import paddle: Imports a custom-defined paddle class for creating and managing paddle objects.
    from ball import Ball: Imports a custom-defined Ball class for creating and managing the ball object.
4. from scoreboard import Scoreboard: Imports a custom-defined Scoreboard class for managing and displaying the score.
5. import time: Imports the time module for pausing the game's execution.

# Setting Up the Screen:

1. screen = Screen(): Creates a new Turtle screen object.
2. screen.setup(width=800, height=600): Sets the screen dimensions to 800x600 pixels.
3. screen.bgcolor("black"): Sets the background color to black.
4. screen.title("PONG Game"): Sets the title of the game window.
5. screen.tracer(0): Disables automatic screen updates for smoother animation.

# Creating Game Elements:

1. scoreboard = Scoreboard(): Creates a new scoreboard object.
2. r_paddle = paddle((350, 0)): Creates a right paddle at the position (350, 0).
l_paddle = paddle((-350, 0)): Creates a left paddle at the position (-350, 0).
ball = Ball(): Creates a ball object.

# Handling Keyboard Input:

screen.listen(): Starts listening for keyboard events.
screen.onkey(r_paddle.go_up, "Up"): Binds the "Up" key to move the right paddle up.
screen.onkey(r_paddle.go_down, "Down"): Binds the "Down" key to move the right paddle down.
screen.onkey(l_paddle.go_up, "w"): Binds the "w" key to move the left paddle up.
screen.onkey(l_paddle.go_down, "s"): Binds the "s" key to move the left paddle down.

# Main Game Loop:

while is_game_on:: Starts a loop that continues as long as is_game_on is True.
time.sleep(ball.move_speed): Pauses the game for a short duration based on the ball's movement speed.
screen.update(): Updates the screen to display the latest game state.
ball.move(): Moves the ball according to its current direction and speed.
Collision Detection:
Checks for collisions with walls and paddles, and adjusts the ball's direction accordingly.
Scoring:
Checks if a paddle missed the ball, resets the ball, and updates the scoreboard.

# Exiting the Game:

screen.exitonclick(): Keeps the game window open until the user clicks on it.
