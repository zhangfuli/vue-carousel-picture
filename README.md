# vue-carousel-picture

> A vue component used for carousel picture

## 安装及依赖

### 本组件用到的依赖包如下
``` bash

# vue-style-loader
npm install --save vue-style-loader

# css-loader
npm install --save css-loader

# node-sass sass-loader
npm install node-sass sass-loader
```

### 安装
### 使用时，仅需执行如下命令
``` bash

npm install --save vue-carousel-picture

```

## demo
    <template>
      <div class="hello">
        <VueCarouselPicture :slides="slides" :inv="inv" :style="styleObject" :name="transitionName1" :target="target"></VueCarouselPicture>
      </div>
    </template>
    
    <script>
      import VueCarouselPicture from 'vue-carousel-picture';
      import Css from 'vue-carousel-picture/dist/vue-carousel-picture.min.css'
      import datu from '../../static/img/datu.jpg';
    
    export default {
      name: 'HelloWorld',
      data () {
        return {
          slides: [{      //图片路径
            src: datu,
            href: ''
          },
            {
              src: datu,
              href: ''
            },{
              src: datu,
              href: ''
            }],
          styleObject: {
            width: '100%',
            height: '400px'
          },
          inv: 1000,    //滑动周期
          transitionName1: 'move',  //渐变方式
          transitionName2: 'fade',
          target: '_blank'
        }
      },
      components:{
        VueCarouselPicture
      }
    }
    </script>
    
    <!-- Add "scoped" attribute to limit CSS to this component only -->
    <style scoped>
   
    </style>

### 参数解释
##### slides 轮播图片的地址为json数组
##### styleObject 轮播图的大小
##### inv 图片切换的周期
##### transitionName1与transitionName2 两种图片切换方式


For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).


