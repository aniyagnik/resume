<template>
 <b-container>
   <div id='container-box-skills'>
      <v-progress-linear
        :color="`${ skill.color }`"
        height="15"
        :value="`${ skill.skill }`"
        striped
        rounded
      ></v-progress-linear>
   </div>
 </b-container>
</template>

<script>
export default {
  name: 'skill',
  props: [ 'skill' ],
  data () {
    return {
    }
  }
}
</script>

<style lang="scss">
#container-box-skills{
  opacity: 0.9;
  padding: 1vw;
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
  min-width:400px;
}
#container-box-skills:hover{
   background-image: linear-gradient(to right top, #2261d6, #0088ec, #00a7e5, #00c0cb, #00d5ac, #00d79d, #00d88b, #00d976, #00cb87, #00bb92, #00ab96, #279b94);
  transition: all 1s;
}
</style>
