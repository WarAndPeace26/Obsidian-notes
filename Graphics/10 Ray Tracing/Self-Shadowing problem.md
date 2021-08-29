# Self-Shadowing problem.
***
### Description
***
The problem's name is self explanatory. Basically, sometimes when the value of *t* is recorded, as it is a floating point value, it is not completely precise. As a result, it could just be a bit off, making the value of *t* return a point that is **inside** the surface of the object, as shown here [[SS-Problem.excalidraw]]

![[Pasted image 20210818193336.png]]

### The solution
***
The epsilon value (sent as a parameter to the intersect object inside the *Objects* loop) will drag the intersection point to *or* out of the surface. Now the value of epsilon (**SHADOW BIAS**) is small so it won't be that much of a displacement but it'll be enough to avoid the ray hitting the *current* object's own surface.