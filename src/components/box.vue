<template>
 <b-container>
   <div id='container-box'>
       <h1 class='display-4 font-weight-bold text-capitalize'>{{ data.heading}}</h1>
       <h2 class='headine'>{{ data.line1 }}</h2>
       <li class='title' v-for='(line,i) in data.summary' :key='i'>{{line}}</li>
       <p class='body-2'>{{ data.title}}</p>
       <p class='caption'>{{ data.content}}</p>
   </div>
 </b-container>
</template>

<script>
export default {
  name: 'box',
  props: [ 'data' ],
  data () {
    return {
    }
  }
}
</script>

<style lang="scss">
#container-box{
  background-color: antiquewhite;
  opacity: 0.6;
  padding-top: 3vw;
  padding-bottom: 3vw;
  padding-right: 10vw;
  padding-left: 10vw;
}
</style>
