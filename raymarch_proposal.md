Ray Marching: The Most Fun You Can Have With a Single "For Loop"!

#Abstract
Ray Marching is a loveable algorithm - much like pin-hole photography, it's a simple machine built from household parts for the sake of creating art.
Using the humble tools of a for-loop and an if-statement, we can simulate the interactions between light and 3D forms to render images and animations.
Once you understand these 10 lines of code, you'll find they're quite malleable and can be bent, broken, and extended in fascinating ways — yielding a fruitful playground for creativity and learning.

#Timeline:

#(1min) Introduction, or, what is ray marching, and why do I like it so much?
Display some pretty art made with ray marching.
Show "the code" (10-15 lines!) without going into meaning, just promise that it will make sense by the end of the talk.
Justify why I think this is a beautiful algorithm worth understanding.

#(1min) Lay down some assumptions and the basic framework
Explain we're going to write a (pure) function of the signature (x,y) => (r,g,b), and run it over all of the coordinates of a grid to create an image.
Drive this home by demonstrating some simple functions and the images they generate, no rays involved.

#(2min) How modeling rays of light can generate an image
Restate the constraints - a function of the aforementioned form (x,y) => (r,g,b)
and refine our goal - to model a single ray of "light" passing through 3D space, in order to calculate how that ray will (or won't) intersect with a shape, and return a pixel color accordingly.

Explain what we'll need to accomplish this:
1) a starting point
2) a direction for our ray to travel along
3) a way to know when we we can stop iterating because our ray has collided with the shape along its path.

#(2min) Signed Distance Functions
As we move away from our "eye" along the ray, we need to know when to stop.
Introduce signed distance functions and present them as a solution to this problem.

#(2min) Put it all together:
Show the ~10 lines of code again, and walk through them using the context we've built and visual aids.

#(2min) Extensions
Examples of directions you can take, like adding time as a third input, calculating normals to improve the lighting model, and constructing intereseting SDFs.
Stress that these /can/ be inspired by modeling the physics of the real world, but can also just be making things up and seeing what you like the look of!


#Intended audience
Graphics programming is usually wrapped up in a lot of linear algebra and GPU quirkiness, but I'm going to explicitly structure the material to avoid those concepts entirely.

The talk will assume some familiarity with programming, 3D cartesian coordinates, and basic vector math (addition, scaling). Additionally, some parts will be easier to understand for people familiar with numerical differentiation and function composition, but these are not required to follow along.
