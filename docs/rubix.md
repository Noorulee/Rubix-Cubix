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