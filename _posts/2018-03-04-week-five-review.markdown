---
layout: post
title: "Week Five Review"
date: 2018--3-05 21:00
categories: Weekly Reviews
---
At the beginning of this week I finished off some things that I to improve on the main menu, these were mainly scaling issues with the UI elements. I built the first version for android and the UI did not scale to the smaller screen of my device, this required some tweaking in Unity and fortunately it is just a matter of changing a setting to allow elements to scale to the screen size and not to maintain a constant pixel size. This should allow the game to look similar across many different sized displays/resolutions/aspect ratios. I can now play a basic game on my phone but the back pieces are hard if not impossible to select while these is no camera rotation.

The majority of the week was spent beginning to implement multiplayer, after some research about TCP and UDP connections I decided that the best solution was to use TCP because of its reliable ordering of packets. The project is a turn based game so does not need the speed benefits of UDP. 

I decided to make my server application in C# to allow easy communication with the C# scripts being used by the Unity project, using a WPF C# application allows me to create a GUI for the server and visualise a message log as well as see how many clients are connected to the server in real time. Following a basic tutorial at https://www.codeproject.com/Articles/1415/Introduction-to-TCP-client-server-in-C
I was able to get the unity client to connect to the server application and have both send a message to each other.

The basic tutorial was very linear and only allowed one message to be sent from the server to the client and back again, this didn't allow for any other message to be sent. I now have changed the server to use queues to constantly listen for incoming messages and add them to a queue to be process, then another thread will process these messages and put them in a reply queue, at which point a final thread will send them out to the appropriate recipients.

To be able to send more robust messages later in the project I created a Message class that can be serialised to a byte array and sent across the socket connection and then deserialised on the other side. This solution does require the upkeep of the same class on the server and client and I'm trying to find a way to keep these two files in sync automatically. Using an Enumerator I can send message types with the message, and eventually the server will be able to perform different actions depending on what message type is received.

During the process of making the multiplayer I have been added to the bibliography religiously when I use a solution to a problem off a site and need to reference some information, this will help later on in the project when I need to see specific problems I faced.

