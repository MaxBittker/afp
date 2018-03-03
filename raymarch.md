Marching Rays, OR, The Most Fun You Can Have With a Single "For Loop"!


* may include physical models

#(1min) Introduction, or What is ray marching, and why do I like it so much?

(show an interesting abstract ray marched image)
Ray Marching is an algorithm for going from a description of a 3D shape to a rectangle of pixel values, aka, rendering an image!

It's also expressible in <30 lines of code:

function ray_march(x, y){
    vec3 ro = vec3(1, 0, 1) * x + vec3(0, 1, 0) * y;
    vec3 rd = vec3(0, 0, 1);
    vec3 color = vec3(0, 0, 0) // Background color

    float t = 0.0;
    for(int i = 0; i < maxSteps; ++i) {
        vec3 p = ro + rd * t;
        float d = length(p) - 0.5; // Distance to sphere of radius 0.5
        if(d < acceptably_close) {
            color = vec3(1.0); // Sphere color
            break;
        }
        t += d;
    }

    return color;
}


... code that you probably can't understand right now, but, in 10 minutes, you will hopefully be able to kinda understand.

And once you have some understanding of this code, the algorithm becomes a extremely fertile playground for tweaking, expirimentation, and learning.
Ray marching is very malleable, and it can be broken, bent, and extended in really creative and fascinating ways.

#(2min) Lay down some assumptions and the basic framework

I want everyone to first understand that in ray marching, the image is formed by running a single function one time for each pixel, in isolation.

This means we're going to write a (pure) function that:
1)    takes in (x, y) coordinates of a pixel
2)    ~~~does some cool stuff~~~
3)    and returns a single (r, g, b) color value

This section is about building an understanding of these three steps, so we can talk about a very special type of function you can write for step #2.

The plan here is to show some pseudocode functions of the signature (x, y) => (r,g,b),
and basically play flash cards with their result (with a slight ramp in complexity)

(x, y) => {
    return (0, 0, 0)
}
black square!

(x, y) => {
    return (1, 0, 0)
}
red square!

(x, y) => {
    return (x, x, x)
}
horizontal gradient!

(x, y) => {
    if( x < y ){
        return (0, 0, 0) // black
    } else {
        return (1, 1, 1) // white
    }
}
diagonal stripe!

(x, y) => {
    if( x² + y² < 0.5 ){
        return (0, 0, 0) // black
    } else {
        return (1, 1, 1) // white
    }
}
a circle!



#(2min) Ok, time to march rays.

we're going to write this function of the form (x,y)=>(r,g,b), that models a ray of light passing through 3d space.
This means we need

1) a starting point
2) a direction for our ray to travel
3) a way to know when we're done 


Human art forgers are in a constant battle with the police. As the detection techniques get better, so do the forgers.
By creating multiple neural networks (a “forger” and a “detector”) and pitting them against each other, we end up with a really good forger!

(2min) Training a GAN
Explain how the GAN training process works using visuals
Show examples of the output getting better as the network trains

(3min) Cool applications of GANs

