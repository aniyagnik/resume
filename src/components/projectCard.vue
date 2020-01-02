<template>
  <div class="box">
      <p class='head headline font-weight-bold text-uppercase text-center'>{{ project.name}}</p>
    <div class='projectcard'>
      <div class='image'></div>
      <div class='details '>
        <p class='title text-uppercase'>{{ project.summary }}</p>
        <p class='subtitle-1 text-lowecase font-weight-light'><a :href="`${ project.github }`">{{ project.github }}</a></p>
      </div>
    </div>
    <p class='foot body-2 font-weight-light'><a :href="`${ project.link }`">{{ project.link }}</a></p>
  </div>
</template>

<script>
export default {
  props: [ 'project' ]
}
</script>
<style lang='scss'>
.box{
  justify-content: center;
}
.projectcard {
    width: 32vw;
    height: 23vw;
    -webkit-transition: all 2s;
    transition: background-image 1s;
}
.image{
  background-image: url('../assets/1.jpg');
  width: 32vw;
  border: 5px solid black;
  height: 23vw;
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}
.projectcard:hover{
  .image{
    display: none;
    transition: all 1s ;
  }
  .details{
    opacity: 1;
    background-color: gold;
    width: 32vw;
    height: 23vw;
    transition: all 1s ;
  }
}
.details {
    padding: 5%;

  opacity: 0;
  border: 5px solid black;
}
.v-application .head {
  margin: 0px;
  width: 32vw;
  background-color: whitesmoke;
  border: 5px solid black;
  justify-content: center;
  border-bottom: 0px;
  padding-top: 4px;
  margin: 0px;
}
.foot {
  width: 32vw;
  background-color: whitesmoke;
  border: 5px solid black;
  justify-content: center;
  border-top: 0px;
  padding-top: 4px;
  padding-bottom: 4px;
}

</style>
