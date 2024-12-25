RC Car Simulation

RC Car Simulation is a simple yet dynamic program written in Processing. The simulation lets you control a virtual RC car that moves smoothly toward a target position when you click anywhere on the canvas. The car's orientation dynamically adjusts as it moves, simulating realistic movement mechanics with a minimalist design.

Features
Mouse-Driven Movement: Click anywhere on the canvas, and the car will smoothly move toward the clicked position.

Dynamic Car Orientation: The car automatically adjusts its angle to face the target as it moves.

Simple Design: The car is visualized with a red rectangular body, black circular wheels, and yellow headlights.

Smooth Movement: The car gradually slows down and stops upon reaching the target.


How It Works
Setup: The car starts at the center of the canvas when the program begins.

Mouse Interaction: Clicking on the canvas sets the target position (targetX, targetY) for the car to move toward.

Movement Mechanics: The car's angle (angle) is calculated using the atan2() function to ensure it points toward the target.
Its position (carX, carY) is updated based on speed and direction. The car stops moving when it gets close to the target position.

Drawing the Car: The car's body is represented by a red rectangle.
Four black circles represent the wheels.Two yellow ellipses depict the headlights.


Usage
Open the code in the Processing IDE.
Run the program by pressing the play button.
Click anywhere on the canvas to make the car move to the clicked position.
File Structure
This project includes the following files:

RCCarSimulation.pde: The main source code for the simulation.

README.md: The documentation for the project.

example.png: A screenshot of the simulation in action (optional).

Controls
Mouse Click: Sets the target position for the car to move toward.

Customization
You can modify the following elements in the code to personalize the simulation:

Adjust the car's speed or stopping sensitivity by tweaking the movement variables in updateCar().
Customize the car’s appearance (body color, wheel size, etc.) by modifying the drawCar() function.
Change the canvas size by adjusting the size() function in the setup() method.

Author
This project was created by Jawad F. Naik as part of the course Elements of Media, taught by Professor Fred Wolflink at the Massachusetts College of Art and Design in Boston, Massachusetts, USA.

License
This project is open-source and licensed under the MIT License. See the LICENSE file for details.

Acknowledgments
Special thanks to the Processing Foundation for their robust IDE and creative coding tools, and to the Massachusetts College of Art and Design for providing a platform for exploration and creativity.
