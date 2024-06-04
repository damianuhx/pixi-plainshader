This is an example function how to create an instance of this filter. 
The filter needs besides the base texture a texture for the heightmap (texture_h) and one for the normal map (texture_n). 
The heightmap must be read from a sprite set to the scene -- this should be changed to pass a texture directly. 

```
function (texture, texture_h, texture_n, options={}) 
   {
    returnfilter = new HeightmapFilter(texture_h, 20, texture, texture_n);
    returnfilter.scale.x=0;
    returnfilter.scale.y=120;
    returnfilter.light=1.0;
    returnfilter.invert=-1.0;
    returnfilter.repeat=1.0;
    returnfilter.normal={x: 0.0, y: 0.0};
    returnfilter.factor={x: 1.0, y: 1.0};
    returnfilter.offset = {x: 0.0, y: 0.0};
    returnfilter.zoom=1.0;
    returnfilter.alpha=1.0;
     return returnfilter;
   }
```
