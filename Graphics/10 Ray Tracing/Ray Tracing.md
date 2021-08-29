# Ray Tracing
***
In Ray Tracing, as discussed before, we go a few steps further than [[Ray Casting]]. In this case, we're concerned about the secondary rays (AKA Shadow rays) too.

## Shading
***
For realistic shading, Ray tracing is a much better algorithm than ray casting. 
[[Shading-Ray Tracing]]

## Reflection
***
When utilizing Shadow Rays, [[Reflection]] becomes an important factor.

## Refraction
***
Not all surfaces are mirrors. [[Refraction]] is necessary for those surfaces.

## Recursion
***
The Reflection and Refraction functions call the same Ray Tracing functions that called them, causing recursions. What if there were two mirrors in front of each other? That'd cause an infinite amount of recursions. [[Stopping Recursion]]

### Ray Tree
***
[[Ray Tree]]