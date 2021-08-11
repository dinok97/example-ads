<h1 align="center">AR.js & A-Frame with Gestures</h1>

Example of using gesture events on AR.js with A-Frame. This work is based on [this example](https://github.com/fcor/arjs-gestures).

Scale and rotate 3D elements from your AR.js scene using `gesture-detector` and `gesture-handler` components.


## Try now!

🚀[Open this sample](https://dinok97.github.io/arjs-with-event/index.html) on your phone and [scan this marker](https://killcloud.nyc3.digitaloceanspaces.com/assets/Hiro_marker_ARjs.png)


## How it works?

`gesture-detector` listens to regular touch events directly on `a-scene` and emits a custom event indicating how many fingers were involved ("one", "two", "three" or "many") and passing some details of the event, like the position, spread and coordinates where user touched the screen. This component was developed by 8th Wall for their A-Frame based demos and can be found [here](https://github.com/8thwall/web/blob/master/examples/aframe/manipulate/gesture-detector.js).

`gesture-handler` adds listeners for custom gesture events, emitted by `gesture-detector`. This component should be placed on the 3D element we want to control and it automaticaly detects if the marker or image is found or lost to ensure the element could only be manipulated if it's actually visible. This component could be customized via properties. Currently supports pinch to zoom and finger spin for rotating the element.
