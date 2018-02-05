---
layout: post
title:  "Week 2 Update"
date:   2018-02-04 00:00:00 -0500
categories: update
---
This week features the beginnings of our project core software and a mockup of our touchscreen UI design.

## Core Software
We began work on our core software which will manage pretty much everything our project does, along with interfacing with the UI to provide a clean user experience. The source code for the project can be found [here][repitile_core]. Currently it is able to load and parse our profile file format (which uses [TOML][toml]) which includes information about the temperature and humidity ranges, along with what time the light will turn off and on.

{% highlight toml %}
name = "Test Reptile"

[temps]
max = 90
min = 85

[humidity]
max = 90
min = 85

[light]
on = 08:00:00
off = 18:00:00
{% endhighlight %}
<sub><i>An example of what a profile file looks like</i></sub>

<br />
The next step here is to implement the structures for managing sensors and actuators to do the actual work, and a system for repeating tasks such as updating temperature and humidity information.

## Touchscreen User Interface

In addition to the core software getting its start, Scott, Seth, and Alex designed a beautiful mockup of the touchscreen UI we'll have. The UI will be responsible for relaying information to the user and allow them to adjust settings such as max and min temps. Here's a few preview images of what we hope the UI can look like:

Current conditions:
![RePitileSystem UI Mockup Current Conditions]({{ "/assets/UX_Snap_01.PNG" | absolute_url }})

<br />
Profile settings:
![RePitileSystem UI Mockup Profile Settings]({{ "/assets/UX_Snap_02.PNG" | absolute_url }})

<br />
New profile:
![RePitileSystem UI Mockup New Profile]({{ "/assets/UX_Snap_03.PNG" | absolute_url }}) 

[repitile_core]: https://github.com/repitilesystem/repitile_core 
[toml]: https://github.com/toml-lang/toml