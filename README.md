# Mower Kata Challenge

##Code Challenge


We need to develop an application that helps in controlling brand new mowers. 
Our company has rolled out brand new robotic mowers that are able to cut the grass and to inspect the terrain with their cameras to identify problems in the green areas.

Our building has a lot of green spaces but for the MVP, we will consider only one single green grass plateau to simply the problem.

A green grass plateau, which is curiously rectangular, must be navigated by the mowers so they can cut the grass and that their on-board cameras can get a complete view of the surrounding terrain to send to the Maintenance Office.

A mower’s position and location are represented by a combination of X and Y coordinates and a letter representing one of the four cardinal compass points (N, E, S, W). 

The plateau is divided up into a grid to simplify navigation. An example position might be 0, 0, N, which means the mower is in the bottom left corner and facing North.
In order to control a mower, Maintenance Office sends a simple string of letters. The possible letters are “L”, “R” and ”M”. “L” and “R” make the mower spin 90 degrees left or right respectively, without moving from its current spot. “M” means to move forward one grid point and maintain the same Heading.
Assume that the square directly North from (X, Y) is (X, Y + 1).


###Input

The first line of input is the upper-right coordinates of the plateau, the bottom-left coordinates are assumed to be 0, 0.

The rest of the input is information pertaining to the mowers that have been deployed. Each mower has two lines of input. The first line gives the mower’s position, and the second line is a series of instructions telling the mower how to explore the plateau. The position is made up of two integers and a letter separated by spaces, corresponding to the X and Y coordinates and the mower’s orientation.
Each mower will be finished sequentially, which means that the second mower won’t start to move until the first one has finished moving.


###Output
The output for each mower should be its final coordinates and heading.


###Test case

####Input Test Case #1:
5 5
1 2 N
LMLMLMLMM
3 3 E
MMRMMRMRRM

####Output Test Case #2:
1 3 N
5 1 E


## Assumptions

- The coordinates (for both `Garden` and `Mower`) are always positive numbers.
- The mower executes the command, and then it will check if the `Coordinate` is valid and empty.
    + If there is any problem when executing the command routine, the mower will stop.
- The application will read the whole configuration and commands from a text file following the given description in the statement.
- An example input file is given in the following path `src/main/java/resources/input.txt`.

# HOW-TO

## Build the project

In the `rootDirectory` execute:

> mvn clean install

## Execute tests

In the `rootDirectory` execute:

> mvn clean test

## Execute the application

In the `rootDirectory/target` execute:

> java -jar mower_challenge-1.0.jar <input_file>

where `<input_file>` is the path to the input file (there is an example in the `resources` directory)