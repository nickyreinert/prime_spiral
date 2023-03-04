***runs best in Google's chrome or similar browsers***

# Prime Spiral 
Prime Spiral puts (prime) numbers on a spiral and marks then with a circle. Most parameters can be animated. The animation can be recorded in WebM-Format. 

This is inspired by the idea of the **[Ulam spiral](https://de.wikipedia.org/wiki/Ulam-Spirale)**. The **Ulam spiral** shows some kind of geometrical symmetry for prime numbers. 

## Calculations
The engine will loop throuhg all integers, starting from 1 (or the one you defined in the settings) up to the upper limit you defined and apply the following formular to draw a spiral on the screen:

    x = centerx + (distortion * ((slope + intercept * angle) + diam) * x_angle);


## General Controls

### Reset
Reloads default settings

### Start recording
***shortcut: s***
Starts the animation and the recording. Press s-key again to stop the recording and download the animation in WebM. 

Only the canvas will be recorded, the parameter-container will be ignored.

### Export
Takes all parameters and adds them to the URL as a GET-parameter. This allows you to share your settings. 

### Hide
***shortcut: Escape***
Hides the parameter-container. Press the escape-key again to show the container.

### Start animation
***shortcut: Enter***
Starts the animation. Press the enter-key again to stop the animation.

### Alpha
***shortcuts: + and -***
Increased or decreases the opacity of the parameter-container.

## Drawing controls

### Animation

#### FPS
Limits the frames per second. Decrease this value to slow down your animation.

***Hint:*** If you want to slow down the animation, you should use the animatable parameters step value. See below.

#### Resolution scale
Controls the resolution of the canvas. This allows you to render more objects to the canvas but also increases required computing power.

#### Do not draw outside the canvas
This will stop drawing elements that are clearly outside the visible area. This could increase performance but also lead to interesting effects. 

### Angualar functions

#### Calculate X and Y angle by...
To calculate the coordinates of the next point of the spiral, we use angular functions that you can select here. 

### Misc
#### Start at center
Move the position of the spiral center to the center of the screen or to the top left. 

#### Power by 2 for angle calculation
If activated, we will take the power of two of the angular value to calculate the coordinate. 

#### Activate distortion
If activated the current number will be taken as a distortion factor.

### Numbers

Allos you to render all numbers or prime numbers to the screen.

### Arcs
#### Show arcs around non-primes
Draw arcs on every non-prime number.

#### Show arcs around prime numbers	
Draw arcs on every prime number.

#### Scale arc diameter	
Scales the arc diamater according to it's distance to the center.

#### Fade out arcs
Adds a fading effect for the background color of the arc. The higher the distance to the center, the higher the opacity of the arc.

#### Lines
#### Use bezier curves
Apply bezier function on the spiral lines.

#### Prime rays from the center	
Draws a line from the center to the prime number. 

#### Prime rays width	
The widht of the prime ray.

#### Prime rays with relative width	
Scales the width of the prime ray according to the distance from the center.

#### Rays fade out	
According to the distance from the center, increase the opacity. 

#### Colors
This area allows you to select colors for the background, arcs and lines. 

## Animatable Parameters

This is the most interesting parts. All parameters listed here can be animated and have an impact on the above mentioned formula. 

The parameters are defined by the actual value (represented by the input field and the range slider), a minimum and a maximum value and a step value.

You may check the checkbox of the parameter, to start it's animation. The animation speed may be controlled with the step value. Most parameters understand a decimal value here (except the range). This allows you to smoothly decrease the animation speed.

Most values can be negativ, too.

### Range
This defines the range of numbers you want to calculate.

### Density
This control the quality aka resolution of the spiral. The more this values approaches 0, the more compact the spiral is and the less "edges" it has. The higher the value, the more the spiral seems to be made out of triangles. 

#### Rotation
This simply rotates the spiral. 

#### Slope
This allows to control the distance between the points (every point represents a number).

#### Intercept
This allows to control the distance of all points to the center. 

#### Divide by Pi
This controls the divisor applied to the angular-value from the above mentioned formula.

#### Main diameter
The diameter of the whole spiral.

#### Marker diamter
The diameter of the little arcs. 
