# Rubix

DRY - Don't Repeat Yourself!
YAGNI - You aren't going to need it

## Task Description

How to solve a rubik's cube!

## Definitions

### What is rubik's cube?

6 faces.
6 colors.
each face has 9 boxes.

Solved State -> All boxes in each face has the same color.

Unsolved State -> Each face does have homogeneous color.
New definition: Any combination of faces which is not of the Solved State!

### How to represent a Rubik's Cube?

#### Defining a box

Each box has a unique color.

Let the colors be <R, G, B, O, W, Y>

Now, each box can be represented by a single letter of color!
For example: R

#### Defining a face

1 face has 9 boxes of same or different colors arranged in a 3x3 grid.

=> A face can be represented by 9 boxes in a particular arrangement.
For example:
R G B
O W Y
R Y O

=> There are 6 faces.

#### Defining a cube

1 cube has 6 faces.
Each face has relation to other faces.

The relation:
Let us number each face as 1..6
Each face has a particular ordering in the cube.

For example:
Face1 | Face2 | Face3 | Face4 | Face5 | Face6
------|-------|-------|-------|-------|-------
R G B | R Y W |
O W Y | O B G |
R Y O | W Y R |

## States

Each box will have the same color within a face is Solved State, otherwise Unsolved
State.


# The algorithm to solve
1. Unsolved State
2. Solved State
3. Unsolved -> Solved State


## Steps to solve Rubix cube

 ## More Details reg CUBE we should know if we take the cube apart and check the component of the cube

 we will notice there are three different type of pieces on the cube

 1. Center Piece >> Each center piece hold one color so because there are 6 center, the color of the center tells u the color of the entire side.
eg >> if the center has red color on it, it means entire side should be red when the cube is solved.

2. The Edge >> it holds 2 color
def edge >> type of piece that fits in between 2 centers.
eg>> any 2 color edge fits between that 2 colors centers.

3. Corner Piece>> it has 3 colors on it
   that corner whichever the colors they have will fits between that 3 colors only.

### Note
Each piece is unique on the cube. There will be only one of each piece.

some cases are not possible
eg>> is that whose center piece is opp. they will not make edge

## How the cube moves?
1. Solve the White Cross

Make a “+” sign on the white face.

The edges (white-blue, white-red, etc.) must match the center colors of their sides.
 Centers never move — they tell you what color each side should be.

2. Solve White Corners

Place the 4 white corner pieces (each has 3 colors) in the right spots.

Algorithm (when white is facing up):
 R' D' R D (repeat until corner is in place)

3. Solve the Middle Layer (Edges)

Now fix the edges in the second layer.

If the target piece goes left:
  U' L' U L U F U' F'

If it goes right:
 U R U' R' U' F' U F

Step 4: Make Yellow Cross

You’ll use this to fix the top layer.

Algorithm:
F R U R' U' F'

(Repeat until a yellow “+” appears)

5. Solve Yellow Corners

Make sure the yellow corners are in the right spots (even if not oriented correctly).

Algorithm:
  U R U' L' U R' U' L

6. Orient the Yellow Corners

Turn the cube so yellow is on top, then:

 R' D' R D (repeat until corner is correct; rotate top to fix next corner)

Step 7: Finish the Last Layer (Edges)

Now just move the last four edge pieces into position.

Algorithm:
 F2 U L R' F2 L' R U F2


















# Representation in a computer

1 box -> Color/Character (R, G, B, W, Y, O)
1 face -> Matrix -> 
face1 = [ 
    [R, G, B],
    [O, W, Y],
    [R, Y, O]
]

face2 = [ 
    [R, G, B],
    [O, W, Y],
    [R, Y, O]
]
.
.
.

1 cube -> 

[, face2, , ]
[face1, face3, face4, face5]
[, face6, , ]