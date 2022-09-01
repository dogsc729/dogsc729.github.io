---
layout: page
title: Bikesla
description: A embedded system device on a bicycle with STM32 IoT Node, connected to iPadOS App via Bluetooth.
img: assets/img/bikesla_background.jpg
github: https://github.com/dogsc729/Bikesla
importance: 1
category: Course Work
---
### Function
1. ***Speed-checking:*** Using the Hall sensor, with the magnets on the wheel, we can calculate the speed of the spinning of the wheel and inference the speed of the bicycle. The method of calculating the speed of the bicycle is:  
   $$ speed = {perimeter \over timediff} $$, where  
   perimeter = The perimeter of the wheel  
   timediff = The difference between two times the magnet passing through the Hall sensor.
2. ***Lock/Unlock:*** Using the App, we can unlock and lock the bicycle.
3. ***Bicycle-finding:***
   1. Using the App, pressing the Flash button to make the LED flicker. It is convenient for finding our bicycle at night.
   2. Press the Ring button to make the buzzer ring for 2 seconds, users can locate where the bicycle is much easily with this function.
   3. There is an additional drop down menu for users to adjust the lightness and the frequency of the LED.
4. ***Speeding detection:*** Based on the speed limit of Palm Avenue, we set the buzzer to ring for 2 seconds if the speed exceeds 20 km/hr.
5. ***Theft alarm:*** If the bicycle is locked, with the Hall sensor on the wheel, if the sensor detects that the wheel spins over some certain criteria, we regard it as abnormal usage, the buzzer will ring continuously.
6. ***Fall detection:*** Using the intrinsic triaxial accelerometer of the STM32 IoT Node, if we detect the z-axis acceleration is less than 500 m/s, we regard it as someone crashed, the buzzer will ring continuously, informing the people nearby.



The method of calculating the speed of the bicycle is:
Every project has a beautiful feature showcase page.
It's easy to include images in a flexible 3-column grid format.
Make your photos 1/3, 2/3, or full width.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/1.jpg" title="example image1" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal it's glory in the next row of images.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
{% endraw %}
