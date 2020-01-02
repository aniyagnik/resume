<template>
 <b-container>
   <div id='container-box'>
       <h1 class='headBox font-weight-bold text-capitalize'>{{ data.heading}}</h1>
       <h2 class='line1'>{{ data.line1 }}</h2><br>
       <li class='summary' style='font-family:arial black' v-for='(line,i) in data.summary' :key='i'>{{line}}</li>
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
  opacity: 0.55;
  padding-top: 3vw;
  padding-bottom: 3vw;
  padding-right: 10vw;
  padding-left: 10vw;
}

.headBox{
  font-size: 5.5em;
}
.line1{
  font-size: 2.2em;
}
.summary{
  font-size: 1.2em;
}
@media only screen and (max-width: 770px) {
  #container-box{
    padding-right: 5vw;
    padding-left: 5vw;
  }
  .headBox{
    font-size: 3.5em;
  }
  .line1{
    font-size: 1.6em;
  }
  .summary{
    font-size: 1em;
  }
}
</style>
