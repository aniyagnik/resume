<template>
 <b-container>
   <div id='container-box-skills'>
       <h1 class='headline font-weight-bold text-capitalize '>{{ skill.lang }}&nbsp;&nbsp;&nbsp;</h1>
        <v-progress-circular
        :rotate="360"
        :size="100"
        :width="15"
        :value="`${ skill.skill }`"
        color="pink"
      >
        {{ skill.skill }}
      </v-progress-circular>
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
   background-image: linear-gradient(to right top, #ebdfe5, #e9d7e5, #e2cfe8, #d6c9ed, #c5c5f2, #b4c9f9, #9fcdfe, #87d1ff, #73dcff, #60e8ff, #58f2fc, #5ffbf1);
  opacity: 0.9;
  padding: 1vw;
  box-shadow: 0px 6px 20px white;
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
}
#container-box-skills:hover{
  box-shadow: 0px 3px 10px gold;
   background-image: linear-gradient(to right top, #2261d6, #0088ec, #00a7e5, #00c0cb, #00d5ac, #00d79d, #00d88b, #00d976, #00cb87, #00bb92, #00ab96, #279b94);
  transition: all 1s;
}
.v-progress-circular {
margin: 1rem;
}
</style>
