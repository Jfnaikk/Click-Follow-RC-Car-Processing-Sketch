RC Car Simulation

This program is a simple RC car simulation written in Processing. The car moves smoothly toward a target location when the user clicks anywhere on the canvas. The movement is calculated using the car's angle and distance to the target. This simulation demonstrates basic movement mechanics and dynamic visualization.

Features

Mouse-Driven Movement: Click anywhere on the canvas, and the car will move smoothly to the clicked position.
Dynamic Car Orientation: The car automatically adjusts its direction to face the target as it moves.
Simple Design: The car has a red rectangular body, black circular wheels, and yellow headlights.
Smooth Movement: The car gradually stops when it reaches the target.
How It Works

Setup: The car is initialized in the center of the canvas.

Mouse Interaction: Clicking sets the target location (targetX, targetY), and the car starts moving toward it.

Movement Mechanics: The car's angle (angle) is calculated using the atan2() function to point it toward the target.
The car moves by updating its position (carX, carY) based on its speed and direction.
The car stops when it is close to the target.

Drawing the Car: A red rectangle represents the car's body.
Four black circles represent the wheels.
Two yellow ellipses represent the headlights.
Usage

Open the code in the Processing IDE.
Run the program.
Click anywhere on the canvas to move the car to the clicked position.

Code Details

Main Functions:
setup(): Initializes the canvas and car properties.
draw(): Continuously updates the screen, handling movement and rendering.
drawCar(): Visualizes the car, including the body, wheels, and headlights.
updateCar():
Handles the car's movement.
Stops the car when it reaches the target.
mousePressed():
Sets the target position when the user clicks.
Activates the car's movement.

Processing IDE (Download from https://processing.org/)
Compatible with any system that can run Processing (Windows, macOS, Linux).
Enjoy experimenting with the RC car simulation! 🚗
