# Shading In Ray Tracing
***
***The first line*** is basically what we get from Ray Casting. Here we're getting the color of the closest object. *Hit* is the intersection point, from there we're getting the Material from which, we're getting the color.

***Line 2*** is a loop that is traversing every light source. So the following instructions will be executed for every light source.

***Line 3*** is working with the secondary ray. Recall that rays are represented with an origin and a direction. Here, the origin is the intersection point *hit* and the direction is the direction towards the current light source.
![[Pasted image 20210818185606.png]]

***hit2*** object is initialized with the *t* value that is the distance from the hit point to the light source.

Now, for every object, a loop will be executed in ***lines 5-6***, where we'll check if the ray2 intersects with any other object. Not, if it does, the value of *t* for hit2 will change when the object is closer to the light source.

```ad-attention

This means the ray is hitting an object before reaching the light source. 
i.e. A shadow is being casted on the initial object
```

Now, in ***lines 7-8***, we're checking if the value of *t* has indeed changed. If it has, the color of of the object will be changed to the shaded version of it. But if the condition is true, then the color will get some lightening because then the object will be brighter.

At the very end, the color is returned.

Now, it's not a happy ending because one more problem needs to be solved. The [[Self-Shadowing problem]]