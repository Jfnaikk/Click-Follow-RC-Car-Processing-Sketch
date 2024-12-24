/* 
 * Date: December 23, 2024
 * Author: Jawad F. Naik
 * Class/Professor: Elements of Media / Fred Wolflink
 * Institution: Massachusetts College of Art and Design
 * Location: Boston, Massachusetts, USA
 * 
 * 
 * Description:
 *
 * This program creates a simple simulation of a red car in Processing. 
 * The car moves smoothly toward a clicked location on the canvas. The
 * program calculates the angle and distance to the target position
 * and animates the car accordingly. 
 */

float carX, carY; // Car's current position
float carWidth = 60, carHeight = 30; // Dimensions of the car
float speed = 2; // Speed of the car
float angle = 0; // Direction (in radians) the car is facing
float targetX, targetY; // Target position for the car
boolean moving = false; // Indicates whether the car is currently moving

void setup() {
  // Set up the canvas and initialize car position
  size(800, 600); // Canvas size (800x600 pixels)
  carX = width / 2; // Start car in the center horizontally
  carY = height / 2; // Start car in the center vertically
  targetX = carX; // Initial target position is the car's starting point
  targetY = carY;
}

void draw() {
  // Draw the background and update/draw the car
  background(200, 220, 240); // Light blue background color
  updateCar(); // Update car position and logic
  drawCar(); // Draw the car
}

void drawCar() {
  // Draw the car at its current position and orientation
  pushMatrix(); // Save the current coordinate system
  translate(carX, carY); // Move to the car's position
  rotate(angle); // Rotate the car to face the target
  
  // Draw the car body
  fill(255, 0, 0); // Red color for the car
  rectMode(CENTER); // Center the rectangle at (0, 0)
  rect(0, 0, carWidth, carHeight); // Draw the car body
  
  // Draw the wheels
  fill(0); // Black color for the wheels
  ellipse(-carWidth / 2, -carHeight / 2, 12, 12); // Top-left wheel
  ellipse(carWidth / 2, -carHeight / 2, 12, 12);  // Top-right wheel
  ellipse(-carWidth / 2, carHeight / 2, 12, 12);  // Bottom-left wheel
  ellipse(carWidth / 2, carHeight / 2, 12, 12);   // Bottom-right wheel
  
  // Draw the headlights
  fill(255, 255, 100); // Yellow color for the headlights
  ellipse(carWidth / 2 + 5, -carHeight / 4, 8, 8); // Top headlight
  ellipse(carWidth / 2 + 5, carHeight / 4, 8, 8);  // Bottom headlight
  
  popMatrix(); // Restore the original coordinate system
}

void updateCar() {
  // Update the car's position and check if it has reached the target
  if (moving) {
    // Calculate the angle to the target
    angle = atan2(targetY - carY, targetX - carX);
    
    // Calculate the distance to the target
    float distance = dist(carX, carY, targetX, targetY);
    
    // Move the car toward the target if it's far enough
    if (distance > speed) {
      carX += speed * cos(angle); // Update X position
      carY += speed * sin(angle); // Update Y position
    } else {
      moving = false; // Stop the car when close to the target
    }
  }
}

void mousePressed() {
  // Set the car's target position to the mouse click position
  targetX = mouseX; // X coordinate of the target
  targetY = mouseY; // Y coordinate of the target
  moving = true; // Start moving the car
}
