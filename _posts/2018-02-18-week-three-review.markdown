---
layout: post
title: "Week Three Review"
date: 2018-02-18 21:00
categories: Weekly Reviews
---
During Week three I had to fix a problem with implementing movement that had been occuring at the end of week 2. When a piece was selected I was using the code for detecting a mouse click with the left mouse button, but in Unity this fires of constantly while the mouse button is being held. Eventhough you press the mouse button for a brief moment, that is enough time to fire several times which results in different Out of Bounds (OOB) exceptions. According to https://stackoverflow.com/questions/44295502/unity-input-detected-multiple-times-in-a-press the correct was to it is to change.

{% highlight c# %}
Input.GetMouseButton(0);
{% endhighlight %}

To

{% highlight c# %}
Input.GetMouseButtonDown(0);
{% endhighlight %}

This simple change fixed the functionality.


The rest of week three consisted of 
