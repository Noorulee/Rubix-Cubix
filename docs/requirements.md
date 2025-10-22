# Requirements

## Functional Requirements
1. show a 3D cube
2. Keyboard keys/mouse to solve the cube
3. zooming and panning 
4. game restart and reset button
5. start with the random cube
6. score, if one face solved we will give intermediate score.
7. timer 

## Technical Requirements
1. Tech Stack Overview
   
3D Cube Visualization   -- Three.js (most popular 3D JavaScript library)
Frontend Framework (optional) -- React.js (for UI, buttons, controls, etc.)
State Management  -- (optional)	Zustand / Redux (if using React)
Styling	--- Tailwind CSS or plain CSS
Algorithm for Solving	-- JavaScript implementation of Kociemba’s algorithm or Beginner layer-by-layer algorithm
Animations / Controls	-- Three.js built-in animations and OrbitControls
Cube Interaction	-- Raycasting in Three.js for face selection and rotation

## How Your Project Will Work

1. User Interface (React or Vanilla JS)

A 3D cube rendered using Three.js.

Buttons for “Shuffle”, “Solve”, “Reset”.

Maybe color pickers to manually input cube colors.

2. 3D Engine (Three.js)

The cube will be made of 27 smaller cubelets (3×3×3).

You’ll use BoxGeometry and MeshBasicMaterial for each cubelet face color.

Use Group objects to rotate layers as a whole.

3. Algorithm Logic (JavaScript)

When the user presses “Solve”, your code reads the cube’s current state.

Run your solving algorithm (you can start with CFOP beginner algorithm).

Then animate the rotations using Three.js transformations.

4. Animation / Interaction

Use OrbitControls for rotating the view.

Use mouse clicks or drag gestures for manual cube rotations.