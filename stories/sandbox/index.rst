.. title: Sandbox
.. slug: sandbox
.. date: 2016-06-16 15:27:17 UTC+02:00
.. tags:
.. category:
.. link:
.. description:
.. type: text

Overview
--------

I worked on this while reading "Introduction to 3D Game Programming with DirectX 11".
While the book is really well written and describes the DirectX API in detail the
example code provided is only useful for very small examples. Because of this my
goal was to build my own application and add the effects described in the book.

Effects
_______

Some of the effects I implemented were:

- Phong shading
- Texturing with diffuse and transparent textures
- Billboards
- Hardware instancing
- Image Blurring
- Tesselation of geometry
- Frustum culling with OBB
- Picking of meshes
- Environment mapping
- Normal and Displacement mapping
- Terrain tesselation
- Particle systems
- Shadow maps

.. image:: /images/sandbox/background.png

Challenges
----------

Starting off
____________

Something I struggled with at the beginning was how to approach the implementation.
At first I started with reading the chapter on one subject and then implementing it
as described in the book. Sometimes that would not really work resulting in an
image clearly wrong but I was not sure where the problem was. Without experience
it can be really hard to debug such problems.

After finishing the project I established a different routine when implementing something new.
I start with the minimal working solution which creates a result on screen. After this
I add more and more features and check if the output is ok. If something is not working
correctly I use tools to verify the implementation.

Tools
_____

For Debugging I found both the Visual Studio Graphics Debugger as well as RenderDoc
really helpful. In general I prefer RenderDoc for several reasons:

- The overview of a frame is divided in passes e.g. depth-only or colour pass
- pipeline state highlighting when something is missing
- buffer content format combinations possible
- overall better layout e.g. inspecting constant buffers while the pipeline state is still shown

Managing effects
________________

One thing I really missed in the book were ideas how to manage all the different effects.
Most of the examples are for one particular effect and the overall framework is designed
with this kind of applications in mind. While this is obviously good to highlight
only the relevant features bringing all together is a completely different story.

Putting everything together
___________________________

The major problem which became apparent during the development was that I was missing
a good structure to organize the drawing of the objects in scene with different effects.
This made it increasingly complicated to add new shader effects as well as add the
information needed to the objects and the drawing of a scene.

Most of this has to be rewritten to be made more scaleable. Ideally the meshes would
be sorted based on the needed effects and then after setting the effect the appropriate
meshes are rendered. At the moment too much is still hard coded making the system not
flexible enough.
