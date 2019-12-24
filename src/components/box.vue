<template>
 <b-container>
   <div id='container-box'>
       <h1 class='display-4 font-weight-bold text-capitalize'>{{ data.heading}}</h1>
       <h2 class='display-2'>{{ data.line1 }}</h2>
       <p class='headline'>{{ data.content}}</p>
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
  margin-right: 20vw;
  margin-left: 20vw;
  padding-top: 3vw;
  padding-bottom: 3vw;
  padding-right: 10vw;
  padding-left: 10vw;
}
</style>
