# Intersections of Ray and Different Types of Objects
***
## Intersection with Plains
***
##### Representation of 3D Plains
***
[[Representation of 3D Planes]]

##### Intersection of Plane and Ray
***
A point where a plane intersects with a ray is both on the plane and on the ray. So,
if the Ray at that point is, 
> P(t) = Ro + t.Rd

The point P should be on the plane too.  
> H(P) = n.P + D =0
> n.(Ro + t.Rd) + D =0
> r = -(D + n.Ro)/n.Rd

```ad-important
title: Some facts about t

1. n.Rd is a dot product of two vectors. The *normal vector of the plane* and the *Direction vector of the ray*. It can be 0 at times when the object's surface and the ray are parallel (Signifying that they meet at Infinity). 
	- In situations where n.Rd = 0, it's handled separately by avoiding a render altogether.
2. For the object to be closest, the Value of t has to be smallest. So t_closest is the goal here. But we also have a t_min, when t is less than that, the obejct is behind the eye and irrelevant to the render
3. [[Shading]] for information on how the Plane will be shaded *(Diffuse Shading)*

```

## Intersection with Spheres
***
##### Representation of a Sphere
***
[[Representation of Spheres]]
##### Intersection of Ray and Sphere
***
For a Ray
> P(t) = Ro + t.Rd

Inserting it into the sphere, we get
> H(P) = P.P - r^2 = 0
> Rd.Rd(t^2) + 2Rd.Ro.r + Ro.Ro - r^2 = 0
```ad-important
title: *t* for a Sphere

following the Quadratic equation ax2 + bx + c = 0, we get
- a = 1 (Rd.Rd = 1; Direction vectors are unit vectors)
- b = 2.Rd.Ro
- c = Ro.Ro - r2

so t = (-b +- d)/2a
where d = (b2-4ac)^(0.5)

```

###### The Possible States of the Determinant d
1. Case 1:
> b2 - 4ac < 0 -> ***No intersection***
2. Case 2:
> b2 - 4ac = 0 -> ***Single Intersection at ***
> >t = -b/2a
3. Case 3:
> b2 - 4ac > 0 -> ***Multiple Intersections at***
> > t = (- b + d)/2a ***&*** (- b - d)/2a

![[Pasted image 20210818001847.png]]

##### Sphere Normal
***
Normal  = Q/||Q||
![[Pasted image 20210818005121.png]]
