# Ray Casting
***
## Concept 1 Rendering:
***
[[Rendering]] is the main objective of Ray Casting. Ray Casting is basically an algorithm used *to render*.

## Algorithm Outline:
***
Basic [[Description]]
## Ray Casting VS Ray Tracing
***
In Ray Tracing we consider *Secondary* rays. 
In the case of Ray Casting, we don't consider the shadow an object may be casting on another. In case of Ray Tracing, however, we trace secondary rays from each object *recursively* back to the light source.
That's why Ray Casting is a simpler, hence faster, algorithm. But for realistic rendering, Ray Tracing is necessary.
```ad-important
title: Ray Tracing VS Ray Casting

*Ray Casting* = Eyes rays only
*Ray Tracing* = Secondary Rays too.

```

## Complex Solid Geometry
***
[[CSG]]
