---
layout: post
title: "Week Three Review"
date: 2018-02-18 21:00
categories: Weekly Reviews
---
During Week three I had to fix a problem with implementing movement that had been occurring at the end of week 2. When a piece was selected I was using the code for detecting a mouse click with the left mouse button, but in Unity this fires of constantly while the mouse button is being held. Even though you press the mouse button for a brief moment, that is enough time to fire several times which results in different Out of Bounds (OOB) exceptions. According to https://stackoverflow.com/questions/44295502/unity-input-detected-multiple-times-in-a-press the correct was to it is to change.

{% highlight c# %}
Input.GetMouseButton(0);
{% endhighlight %}

To

{% highlight c# %}
Input.GetMouseButtonDown(0);
{% endhighlight %}

This simple change fixed the functionality.

Once the generation of the movement tiles had been fixed by correctly orienting the compass directional system I was using, I then had to move each piece when a tile was selected. I hoped to implement an animation that moves the piece from its original position to the selected position, but that feature is not high priority at the moment. The pieces do however now instantly move to the location of the tile selected and then become deselected, although I did have a problem where the piece had only moved visually there was still a reference on the array relating to the initial position of the piece. This meant that other pieces and the piece that just moved could never go onto or over a space that was originally occupied at the start of the game. This was fixed quite quickly and now movement works as intended, including not allowing normal pieces to be able to move on to the corners but the king can.

I also created this github.io blog to allow me to collect all of my thoughts over the project together and organise my ideas.
I am still trying to find an effective way of curating the ideas and features for the project.
