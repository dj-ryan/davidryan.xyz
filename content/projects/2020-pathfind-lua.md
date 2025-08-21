+++
title = "Pathfind Lua"
date = 2020-01-01
template = "post.html"
draft = false

[extra]
description = "General pathfinding project using C++, Lua, and Gdscript with different algorithms and varying degrees of success"
+++

# Pathfind Lua
## Table of Contents
- [Overview](#overview)
- [Chernobyl](#chernobyl)
- [Lua Script](#lua-script)
- [Documents and Code](#documents-and-code)
## Overview
This is a very general project to approach the problem of node path finding. I use several different languages including C++, Lua, and Gdscript and have several different programs with different functionality and varying degrees of success.

![A* Search Algorithm](/a_-search-algorithm-1-removebg-preview.png)
## Chernobyl
### Wednesday July 22, 2020
Using C++ and map functionality, there is a much more complete way to calculate the number of moves it will take to get to a particular tile. Instead of calculating the number of steps based on the two points which would not take into account any obstacles in between the points, it is better to start at the origin and step outwards in every possible direction, recording the number of steps. This method allows for obstacles of irregular shape to be considered.

This method is implemented in Chernobyl. There is a master map of all coordinate values represented in a pair container. Mapped to each coordinate, there is a step value. The program starts at the origin and then proceeds to check the nodes above, below, to the right, and to the left of it. If these nodes are part of the master map and they do not already have an assigned value, the current step count is saved, and the point is saved into another map where all previous points are saved. At the end of the loop, the previous points map is saved in a current points map, and the step counter is increased. The loop then starts at the top of the current points map and completes the same procedure for each node.

This will then step through each possible node on the map. When encountering an obstacle, the algorithm simply steps around the edge and records the proper step value.

This creates a singular heat map that all other entities can use to path find towards or away from the origin using simple logic. The algorithm is far from being efficient. It can complete 25600 node calculations in just under 1000ms on a 3GHz processor.

- **Github Repo:** [link](https://github.com/dj-ryan/PathFind-Chernobyl.git)

## Lua Script
### July 2020
The main inspiration behind writing this in Lua script was to be able to port it over to a game called Crayta. This script is able, when given a matrix, a player position, and a goal position, to find the shortest route to the goal. It handles any number of convex obstacles such as a square or circle. The basic functionality of the algorithm calculates a heat map based on the distance from all tiles to the goal. This is calculated using the coordinates of the goal and the coordinates of the tile. Then some very basic movement logic chooses the largest value of all neighboring tiles. Any obstacles are given a value of 0 and are therefore never chosen.

The problem arises when trying to handle concave shapes when the player starts inside the obstacle or the goal is inside the obstacle. This is because the heat map does not take into account backtracking. It only calculates the raw distance from the goal.

The solution that I have begun developing is treating the open end or the "entrance" of the concave obstacle as an intermediate goal. Once this has been reached, a new value matrix is calculated on the inside of the obstacle, and the process is repeated.

- **Github Repo:** [link](https://github.com/dj-ryan/PathFind-Lua.git)

## Documents and Code

Last Modified: 7/29/2020

**Contact:**
David Ryan
[davidryan@davidryan.info](mailto:davidryan@davidryan.info)

&copy; Copyright 2020 [davidryan.info](davidryan.info)