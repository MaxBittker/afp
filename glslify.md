require('WebGL-magic') with glslify

https://mattdesl.svbtle.com/glslify

Abstract:

Intrigued by WebGL? Don't go at it alone! Leverage the bundling tool glslify to get your pixels flowing. I'll introduce you to glslify and its ecosystem of friendly micro-libraries for the GPU that will empower you to learn graphics programming and build things that will make people on the internet say "neat". Pick up the tools you need to soar beyond "hello world".

Details:

This talk is aimed at people who are interested in learning WebGL, or have tried to learn but were repelled by the oblique api and the intimidating rawness of the environment once they had things set up.

WebGL is unwelcoming to newcomers. The underlying reality of dealing with GPUs means that even experienced programers will come to the table with some flawed assumptions. I'm going to start with definitions of four core concepts

    Shader: A program written in GLSL that goes from a set of inputs to an output such as vertex position or pixel color.
        (show a short shader animating something cool)

    GLSL: the language that ultimately gets executed on the GPU. It's approximately a C++ subset, and you basically write a function that outputs the color for a single pixel, but massively in parallel. The restrictions are pretty interesting, and reflect the hardware it runs on.
        (show some syntax, show example of restrictions on control structures and heap usage.)

    WebGL: set of JS APIs to talk to the GPU. Includes creating buffers, compiling shaders, and sending data from JS into the shader.
        (show example, they're ugly)

    GLSLify: A tool that implements `require` for GLSL, and allows you to use awesome libraries from npm. Easily importing libraries allows you to build cool things and makes shader construction a lot more *discoverable* and manageable.
        (show an example of a cool metaball or something)

The experience of learning to navigate this new set of concepts and primitives is difficult, and it's made worse by the bizarre layers of ceremony posed by the WebGL apis.

Most programers have some level of peace with the experience of dipping their toes into a new concept by copy/pasting boiler plate from a blogpost. WebGL's is worse than most (Writing C++ inside javascript strings? WTF) but it's just table-stakes.

Once you've got hello world*...
    *(surprise! In webgl, there's no printing, so hello world is pronounced "ugly gradient")

the next step is... Linear algebra?
 😭😞😞😞
 😞😭😞😞
 😞😞😭😞
 😞😞😞😭

It's easy for the stack of new things you're learning to get deep and muddy before you're able to get any payoff or have any fun writing shaders.

A common practice when writing shader code is to find old blogposts explaining topics, copy/paste example code, and then massage it to work in your context. This can be a successful way to learn, but it can also be frustrating. GL has a lot of compatibility edge cases, and debugging them is hard for a newcomer.

This is why I want to show you how GLSLify can serve as vital piece of scaffolding for your WebGL exploration.

Having an awesome package manager and ecosystem is a big part of what makes javascript powerful and fun. Leveraging libraries not only allows you to build cool software more quickly, but it also acts as a guided tour through good practices, possibilities, and points of inspiration. Don't code alone!

I'm going to go through a few examples of things you might want to build with WebGL, and show how the GLSLify ecosystem helps to break them down the domain into helpful, digestible chunks.

Hero Animation for a website:
    glsl-raytrace 
    glsl-sdf-primitives

Video Effects:
    glsl-ascii-filter
    glsl-hash-blur
    glsl-luma

Data Visualization:
    //todo, list packages

Crunch numbers on the GPU, no graphics involved!
    //glsl-read-float


The central thesis is that glslify is a simple, approachable build step that takes much of the pain out shader development, and that exploring and leveraging the ecosystem and community of packages makes the entire process more discoverable.


Pitch:

This is a talk that will shine light on a quirky and misunderstood corner of the web ecosystem, and show how our friendly neighborhood package manager can help make it an expressive and productive experience, without months of study. People will walk away with a better understanding of WebGL, and feel empowered to learn and build WebGL using the glslify ecosystem. I'm also going to stress themes of how library sharing and concept chunking make complicated domains more fruitful and fun.



I've made a lot of art, games, and experiments with the WebGL, regl, and glslify ecosystem. I've taught WebGL concepts informally to friends, and enjoy the way GPU coding has given me a different perspective on programming in general.

Some examples:
https://maxbittker.github.io/webcam-sketches/slowlinescan/
https://maxbittker.com

I've also published small glslify packages (glsl-fractal-brownian-noise & glsl-voronoi-noise)

