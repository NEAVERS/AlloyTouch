﻿English | [简体中文](./README_CN.md)

# AlloyTouch

Smooth scrolling, rotation, pull to refresh and any motion for the web.

# Install
```js
npm install alloytouch
```

# API
```js
new AlloyTouch({
            touch:"#wrapper",
            vertical: true,
            target: target, 
            property: "translateY", 
            min: 100, 
            max: 2000, 
            sensitivity: 1,
            factor: 1,
            spring: true,
            step: 45,
            change:function(value){  },
            touchStart:function(evt, value){  },
            touchMove:function(evt, value){  },
            touchEnd:function(evt, value){  },
            tap:function(evt, value){  },
			pressMove:function(evt, value){  },
            animationEnd:function(value){  } 
 })
```
# Demo(Mobile)

- Simple : [http://alloyteam.github.io/AlloyTouch/](http://alloyteam.github.io/AlloyTouch/)
- 3D : [http://alloyteam.github.io/AlloyTouch/example/3d.html](http://alloyteam.github.io/AlloyTouch/example/3d.html)
- Rotate : [http://alloyteam.github.io/AlloyTouch/example/rotate.html](http://alloyteam.github.io/AlloyTouch/example/rotate.html)
- Carousel : [http://alloyteam.github.io/AlloyTouch/example/carousel.html](http://alloyteam.github.io/AlloyTouch/example/carousel.html)
- Carousel2 : [http://alloyteam.github.io/AlloyTouch/example/carousel2.html](http://alloyteam.github.io/AlloyTouch/example/carousel2.html)
- Three.js : [http://alloyteam.github.io/AlloyTouch/example/threejs/](http://alloyteam.github.io/AlloyTouch/example/threejs/)

## Vue1 & Vue2 Version

### Demo(Mobile)

- ScrollList Vue1: [http://alloyteam.github.io/AlloyTouch/vue/example/](http://alloyteam.github.io/AlloyTouch/vue/example/vue1)
- ScrollList Vue2: [http://alloyteam.github.io/AlloyTouch/vue/example/](http://alloyteam.github.io/AlloyTouch/vue/example/vue2)

```html
<div id="wrapper" v-alloytouch="{options: options, methods:{animationEnd: onAnimationEnd}}">
      <div id="scroller" class="alloytouch-target">
            <ul>
            ...  
            </ul>
      </div>
</div>
```
```js
new Vue({
      el: '#page',
      data: {
            options: {
                  touch:"",//dom for touching
                  target: '#scroller', //dom for transform
                  vertical: true,
                  property: "translateY",  
                  sensitivity: 1,
                  factor: 1,
                  min: window.innerHeight - 45 - 48 - 2000, 
                  max: 0, 
                  step: 40
            }
      },
      methods: {
            onAnimationEnd(){
                  console.log('onAnimationEnd')
            }
      },
      //dynamic set property
      //min: xxx,
      //max: xxx
});
```

# Many thanks to 
- [transformjs](http://alloyteam.github.io/AlloyTouch/transformjs/)

# Who is using AlloyTouch?

![preview](http://sqimg.qq.com/qq_product_operations/im/qqlogo/imlogo.png)

# License
This content is released under the [MIT](http://opensource.org/licenses/MIT) License.
