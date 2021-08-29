# Camera Description
***
The eye/Camera has four quantities that are needed for the algorithm:
> 1. Eye Point (e) -> **Center***
> 2. Orthobasis u, v, w -> (Representing the 3 axes)
> 3. Field of View -> **Angle**
>  4. Image Rectangle -> **Aspect Ratio**

### Coordinates
***
The image is traversed using the image coordinates for convenience. The image, regardless of its aspect ratio, has normalized coordinates in the image plane/rectangle. In both X and Y axes, the coordinates are from -1 to 1, inclusively.

![[Pasted image 20210817131543.png]]


### Perspectives
***
|     | Perspective Projection                                                                | Orthographic Projection                      |
| --- | ------------------------------------------------------------------------------------- | -------------------------------------------- |
| 1   | The parallel lines of the scene converge.                                             | The lines remain parallel                    |
| 2   | The image is seen as if the viewers eyes were located at the center of the projection | Objects appear in their right shape and size |
| 3   | Vanishing points and perspective foreshortening                                       | Those characteristics are not seen here      |
|     |                                                                                       |                                              |
