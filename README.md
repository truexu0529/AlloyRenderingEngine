# AlloyRenderingEngine
Super fast HTML 5 2D rendering engine , supporting Canvas and WebGL rendering

* [website](http://alloyteam.github.io/AlloyRenderingEngine/) 
* [api](http://alloyteam.github.io/AlloyRenderingEngine/doc/)

# Demos
* [bitmap](http://alloyteam.github.io/AlloyRenderingEngine/showcase/bitmap.html) 
* [cache](http://alloyteam.github.io/AlloyRenderingEngine/showcase/cache.html) 
* [filter](http://alloyteam.github.io/AlloyRenderingEngine/showcase/filter.html) 
* [particle](http://alloyteam.github.io/AlloyRenderingEngine/showcase/particle.html) 
* [particlesystem](http://alloyteam.github.io/AlloyRenderingEngine/showcase/particlesystem.html) 
* [particleeditor](http://alloyteam.github.io/ParticleEditor/)
* [shape](http://alloyteam.github.io/AlloyRenderingEngine/showcase/shape.html) 
* [sprite](http://alloyteam.github.io/AlloyRenderingEngine/showcase/sprite.html) 
* [transform](http://alloyteam.github.io/AlloyRenderingEngine/showcase/transform.html) 
* [txt](http://alloyteam.github.io/AlloyRenderingEngine/showcase/txt.html) 
* [box2d](http://alloyteam.github.io/AlloyRenderingEngine/showcase/box2d.html) 

# Tutorials
* [lesson1](http://www.cnblogs.com/iamzhanglei/p/4306146.html)

# Usage
To achieve this effect:

![usage](https://raw.githubusercontent.com/AlloyTeam/AlloyRenderingEngine/master/asset/img/usage2.gif)

You need to use the following code:

```javascript
var bmp, stage = new Stage("#ourCanvas");
bmp = new Bitmap("img/atLogo.png");
//（0.5,0.5）==〉The center is the point of rotation
bmp.originX = 0.5;
bmp.originY = 0.5;
//bind click event, the event monitor can be accurate to pixel
bmp.onClick(function () {
    //apply a random filter to the bmp
    bmp.setFilter(Math.random(), Math.random(), Math.random(), 1);
});
//add object to stage
stage.add(bmp);

var step = 0.01;
//loop
stage.onTick(function () {
    bmp.rotation += 0.5;
    if (bmp.scaleX > 1.5 || bmp.scaleX < 0.5) {
        step *= -1;
    }
    bmp.scaleX += step;
    bmp.scaleY += step;
});
```

# Contact
If you’re interested in AlloyRenderingEngine then feel free to follow me on twitter ([@iamzhanglei](https://twitter.com/iamzhanglei)) .

This content is released under the (http://opensource.org/licenses/MIT) MIT License.
