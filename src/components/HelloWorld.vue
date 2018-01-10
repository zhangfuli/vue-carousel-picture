<template>
  <div class="">
    <carousel :slides="slides" :inv="inv" :style="styleObject" :name="transitionName1" :target="target"></carousel>
  </div>
</template>

<script>
  import carousel from './VueCarouselPicture.vue'
  import datu from  '../assets/img/datu.jpg';
  export default {
    name: 'hello',
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
    components: {
      carousel
    }

  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  h1, h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
  .wrapper{
    width: 70%;
  }
  @media screen and (min-width:769px){
    .wrapper{
      width: 60%;
    }

  }
</style>
