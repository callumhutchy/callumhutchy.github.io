---
layout: post
title: "Week Two Review"
date: 2018-02-11 21:00
categories: Weekly Reviews
---
With the board and pieces being created in week one this meant the logical step was to implement selecting pieces and movement. Selecting pieces was trivial and in Unity a simple mouse over event on all the pieces allows me to know if the mouse is over a certain piece, then a mouse click will allow the selection of the piece being hovered over. I created separate materials for each piece to allow the user to see when a piece had been selected, and implemented a variable to allow the game to know which piece was selected, this also helped get pieces to change colour when they were deselected.

During this week I focused on writing the Outline Project Specification with is a starting overview of the project designed to outline the major features of the project, what I hope to achieve and be able to deliver by the end of the time. My research in week one gave me a good understanding of the game so I feel I should be able to implement it in Unity.

Once pieces were able to be selected I then need to allow the user to move, this could have been done by just letting them click on any tile. The problem with that is if the tile they select was not a possible move they would have no way of knowing that initially. Instead I made the selection easier by generating a series of small glowing tiles on the places where the selected piece can move, this would enable moving the piece easier as I know where they have selected. Unfortunately I was finding it hard generating the tiles in every direction, the system I was using was a 4 way north,east,south and west system where a for loop would run until it found a piece blocking the way of it found the edge of the map. There are still ongoing problems and they will need to be fixed next week  to allow the movement tiles to generate correctly.