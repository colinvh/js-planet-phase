# js-planet-phase

This JavaScript library can be used to draw somewhat realistic lunar or planetary discs, complete with phase shadows:

![example](http://codebox.org.uk/graphics/planet-phase-example.png)

The library requires that browsers support the CSS `border-radius` and `box-shadow` properties, which means it [should work everywhere except IE8 (and earlier)](http://caniuse.com/#feat=css-boxshadow).

To use the library, just include the [planet_phase.js](https://github.com/codebox/js-planet-phase/blob/master/planet_phase.js) file somewhere in your page, and call the `drawPlanetPhase` function once for each disc that you want to draw.

The simplest way to call the function is like this:

<pre>drawPlanetPhase(document.getElementById('container'), 0.15, true);
</pre>

*   The first argument is the HTML element that you want to contain the disc.
*   The second argument must be a value between 0 and 1, indicating the phase:
    *   0.00 = new moon
    *   0.25 = waxing crescent
    *   0.50 = first quarter
    *   0.75 = waxing gibbous
    *   1.00 = full moon
    *   1.25 = waning gibbous
    *   1.50 = third quarter
    *   1.75 = waning crescent
*   The function also accepts an optional third argument, containing configuration values which change the size, colour and appearance of the disc:
    *   `shadowColour` - CSS background-colour value for the shaded part of the disc
    *   `lightColour` - CSS background-colour value for the illuminated part of the disc
    *   `diameter` - diameter of the disc in pixels
    *   `earthshine` - a number between 0 and 1, specifying the amount of light falling on the shaded part of the disc (0 = none, 1 = full illumination)
    *   `blur` - amount of blur on the terminator in pixels (0 = no blur)
