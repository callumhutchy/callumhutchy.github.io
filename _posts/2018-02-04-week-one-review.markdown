---
layout: post
title: "Week One Review"
date: 2018-02-04 21:00
categories: Weekly Reviews
---

During the first week I have researched about the game that I will be making in the project, the game Hnefatafl is a medieval Scandinavian board game. Detailed information about the varieties of games can be found here http://www.gamecabinet.com/history/Hnef.html this site outlines several different ways the game is played depending on geographical location and time period. My project will focus on the 11x11 variety, with 24 barbarians and 12 knights + a king.

The rules of the game are straight forward, all pieces even the king move like rooks in chess, straight lines as far as you want but they can not go over other pieces. When I regular piece has an enemy on two opposite sides they are taken. The king must be trapped on all 4 sides to capture him, although the sides count as a piece so you can pin him with only 3 barbarians. The objective of the kings side is to reach one of the four corners.


Once I had researched enough about the game to understand how to play, I started creating some basic game elements such as a board that generates depending on the size that you want. This variable changing board may not be necessary if I decide to only include 11x11 as the size of the board, the code does handle creating a chequered cream and brown pattern and identifying the corners and the center square of the board.

On the different sized boards there are different ways the pieces can be setup, so this will have to be hard coded for each board type that the player game use. For now I have generated some cuboid pieces in the typical positions on an 11x11 board, more setups may need to be added in the future if different board sizes are added to the final game.