# Ray Casting Skeleton
***
```
For every pixel
	Construct a ray from the ***eye***
	For every object in the scene
		Find intersection with the ray
		keep if closest
			shade
```

![[Pasted image 20210817084023.png]]

For an **X** by **Y** aspect ratio. The ***eye*** will create X times Y rays. Each ray will encounter the *objects* present in the *scene*. And the *pixel* the ray belongs to will be colored based on the **Shading** of the object.

```ad-seealso
title: See also

Shading; It's an important concept.

```
[[Shading]]
> > > > The main pillar of Ray Casting is finding the *Intersection point* and *Normal Vector*

But before that, we have to explore [[Representation of Rays]]

## Generating Rays on a 2D Scenario
***
[[Ray Generation]]

## And after that come the intersections

[[Intersections of Ray and Different Types of Objects]]