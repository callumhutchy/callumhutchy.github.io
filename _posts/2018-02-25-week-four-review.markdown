---
layout: post
title: "Week Four Review"
date: 2018-02-26 21:00
categories: Weekly Reviews
---

I'm a day late with this weekly review because I've been working hard over the weekend to implement the taking of pieces before Tuesday's meeting. As of now all pieces can be taking including the king, as well as this basic debug messages will show you if either team has won, this will be improved in the near future before the mid project demonstration to allow a more friendly user experience and to allow the standalone build to display a victor. 

The game loop has been added so that each team must take turns, you can not select a piece from the same team that has just moved and it gives control over to the other team. This means with the taking of pieces that a game can technically be played on one device with two people. There is not a win state currently that allows the Vikings to win by taking all of the barbarians, but this is a highly unlikely scenario and i'm still unsure if this is a valid win scenario.

The main menu now allows basic functionality and allows a two player game to be created and the two players can decide which team they are. Naturally at this time Player1 goes first, so this must be decided outside of the game, a feature can be added to randomise the first player or something like a game of rock paper scissors can allow one person to decide.

Some technical updates, to aid in the taking of pieces the positions of all pieces are now stored in Lists<Vector2> instead of an Vector2[] this allows for much easier manipulation of the data and saves me making long array manipulation methods which lead to errors if not implemented correctly. The lists implementation is not necessarily faster than an array since the methods that I would have had to create are also being using in the lists, but they are already designed for me.

