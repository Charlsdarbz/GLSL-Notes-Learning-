# What le fuck does OpenGL do!

OpenGL allows us to work with Triangles
a Triangle is made up of 3 Points 😮! Which are called Vertices.
Each vertex has a position in 3 directions.
The directions are called: X, Y, and Z.
The X direction is Left and Right
The Z direction is Forwards and Backwards
The Y direction is Up and Down

By selecting a number for x, y and z this will position the vertex,
in what we call world space

before it can be shown on a computer, table, or phone screen,
The verticies need to be projected onto a 2D screen inside of the Three Vertices.

Once we know the positon on the screen the triangle needs to be colored.
This could just be by just filling in all the pixels inside the triangles verticies
with a simple color or it could require placing a part of a bitmap in the Triangle
or it could involve calculating these colors by adjusting them based on the amount of
light that hit them.

There are 2 stages that go into the process of rendering a triangle.

Step one is to Position the Vertices
Step Two is to then Paint the Pixels

A GLSL Shader Comes in two parts that echo the process
theres a **Vertex Shader** Its job is to take the vertex model coordinates and position stuff on the screen
The vertex shader is called for every vertex in a model.
and then the second part is a **Fragment shader** which is called for **each pixel** and the output of the fragment shader
is in R.G.B.A (Red, Green, Blue, Alpha) format.

The R.G.B.A has a value **between 0 and 1** for each channel a value for example of RGBA(1,1,1,1) would show a white pixel.
while RGBA(1, 0, 0, 0.5) whould show a semi-translucent red on the screen.

on a complex 3D screen something infront of another item would overwrite the pixel color calculated by another shader.
Z'd Buffering takes care of this, The Z'd Buffer representing the distance from the camera calculated by a previous shader the renderer handles this for us. Only thing that we need to be concerned about is what our current shaders should do with the vertices of our model and how the pixels should be colored.


