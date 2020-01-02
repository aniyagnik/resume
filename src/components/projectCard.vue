<template>
  <div class="box">
      <p class='head headline font-weight-bold text-uppercase text-center'>{{ project.name}}</p>
    <div class='projectcard'>
      <div class='image'></div>
      <div class='details text-center'>
        <p class='subtitle-1 font-weight-black red darken-3 white--text'>{{ project.summary }}</p>
        <p class='subtitle-1 font-weight-light'>
          <kbd>github link</kbd>&nbsp;
          <code><a :href="`${ project.github }`">{{ project.github }}</a></code>
        </p>
      </div>
    </div>
    <p class='foot subtitle-1 font-weight-light text-center'>
      <kbd>site link</kbd>
      <code><a :href="`${ project.link }`">{{ project.link }}</a></code>
    </p>
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
  border: 5px solid crimson;
}
.projectcard {
  background-color: rgb(255, 255, 255);
    width: 32vw;
    height: 23vw;
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
  .details{
    opacity: 1;
    transition: opacity 1s ;
  }
  .image{
    display: none;
  }
}
.details {
  background-color: rgb(255, 255, 255);
  position: relative;
  padding: 5%;
  width: 32vw;
  height: 23vw;
  opacity: 0;
  border: 5px solid black;
}
.v-application .head {
  margin: 0px;
  width: 32vw;
   background-image: linear-gradient(to right top, #4e4e4e, #545357, #585960, #5d5f6a, #606574, #657286, #688098, #688eaa, #63a8c5, #59c4db, #54e0ea, #5ffbf1);
  border: 5px solid black;
  justify-content: center;
  border-bottom: 0px;
  padding-top: 4px;
  margin: 0px;
}
.v-application .foot {
  width: 32vw;
   background-image: linear-gradient(to right top, #4e4e4e, #545357, #585960, #5d5f6a, #606574, #657286, #688098, #688eaa, #63a8c5, #59c4db, #54e0ea, #5ffbf1);
  border: 5px solid black;
  justify-content: center;
  border-top: 0px;
  padding-top: 4px;
  padding-bottom: 4px;
  margin: 0px;
}

</style>
