Simple Tween JS
=================

Simple Tween JS is a tiny microframework for easily integrating Tweens by dropping in a file. The performance is uber optimized and has a minimal impact on your application. Its originally designed for HTML Canvas JavaScript applications, but you can use it for just about anything JavaScript related.

Live demo at http://ashblue.github.com/simple-tween-js/ (demo broken in IE9, but
the library does work and has been tested in IE9)

##Setup

1. Download the minified or regular tween.js file and place it in your project files
2. Include the tween script at the bottom of your page, before your other JavaScript files

    ```
    <script type="text/javascript" src="tween.min.js"></script>
    ```
3. You can now create new tweens with syntax similar to the following.

    ```javascript
    var myTween = new Tween(startValue, distance, duration, animationType, loop);
    ```

##Browser Support
Known to be stable in the following browsers. Could very well work in older versions
such as IE8, haven't tested. Mainly because the demo is written in HTML5's Canvas.

* Google Chrome - 22+
* Safari - 6+
* Firefox - 15+
* Internet Exploror - 9+
* Opera - 12+

##Usage Guide
1. Create a new Tween object

    ```javascript
    var myTween = new Tween(startValue, distance, duration, animationType, loop);
    ```

2. You can then get the tween's current value by calling getValue

    ```javascript
    myTween.getValue();
    ```

3. For more information please see the documentation built into https://github.com/ashblue/simple-tween-js/blob/master/tween.js

###Available Methods
* Tween.getValue();
* Tween.expired();
* Tween.reset();
* Tween.set(startValue, distance, duration, animationType, loop);

###Easing Options
You can choose from many different easing options for animationType: 'linear', 'quadIn', 'quadOut', 'quadInOut', 'cubeIn', 'cubeOut', 'cubeInOut', 'quartIn', 'quartOut', 'quartInOut', 'quintIn', 'quintOut', 'quintInOut', 'sineIn', 'sineOut', 'sineInOut', 'expoIn', 'expoOut', 'expoInOut', 'circIn', 'circOut', 'circInOut'

###How to make your tweens process faster
The library here uses Date.now() to get the current time. If your JavaScript application
already has a cached value of the current time, you can substitute all references to Date.now()
with it.
