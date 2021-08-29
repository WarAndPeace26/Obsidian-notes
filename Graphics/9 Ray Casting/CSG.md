# Complex Solid Geometry
CSG is the technique of creating Complex objects from simpler ones.

## Naive Approach to implementing CSG
![[Pasted image 20210818005753.png]]

## Efficient Approach (Using Intervals)
![[Pasted image 20210818005805.png]]

We can decide on entry/exit points by the angle between normals of the intersection points and the ray's direction.
- An Obtuse angle would mean an entry point.
- An acute angle would mean an exit point.
-**N.B:** Directions are considered here.