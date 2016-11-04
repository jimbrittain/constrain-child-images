# constrain-child-images SCSS mixin
`constrain-child-images(`*constraint*`,` *dominant*`)`;
The constraint and dominant can be *'width'*,*'height'* or *'both'*. The constraint keeps the child-images to the width and/or height of the parent, and the dominant is a helper for older browsers that if the possible images have a bias towards portrait or landscape orientations, then by specifiying this, the mixin gives the best chance of not deforming the child-image (maintaining aspect-ratio). This requires the browser to support `object-fit` and `object-position` properties.
# Usage
```
    selector {
        @include constrain-child-images('width', 'width');
    }
```
## Issues
* If a constraint of both is used, then deformation is likely in older browsers
* Need proper browser tests and logging
## Requires
* \_\_object-fit (mixin)
* \_\_object-position (mixin)
