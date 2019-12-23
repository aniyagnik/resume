<template>
 <b-container>
   <div id='container-box'>
       <h1>{{ data.heading}}</h1>
       <h2>{{ data.line1 }}</h2>
       <p size='2em'>{{ data.content}}</p>
   </div>
 </b-container>
</template>

<script>
export default {
  props: ['data']
}
</script>

<style lang="scss">
#container-box{
  background-color: antiquewhite;
  opacity: 0.6;
  margin-right: 10vw;
  margin-left: 10vw;
  padding-right: 10vw;
  padding-left: 10vw;
}
</style>
