<template>
  <div class="box">
      <p class='head headline font-weight-bold text-uppercase text-center'>{{ project.name}}</p>
    <div class='projectcard'>
      <div class='image'></div>
      <div class='details text-center'>
        <p class='summ subtitle-1 font-weight-black white--text'>{{ project.summary }}</p>
        <p class='link subtitle-1 font-weight-light'>
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
  background-color: #c5fcee;
    width: 27vw;
    height: 20vw;
}
.image{
  background-image: url('../assets/1.jpg');
  width: 27vw;
  border: 5px solid black;
  height: 20vw;
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}
.projectcard:hover{
  .details{
    opacity: 1;
    width: 27vw;
    height: 20vw;
    padding: 5%;
    transition: opacity 1s ;
    .summ{
      display: block;
    }
    .link{
      display: block;
    }
  }
  .image{
    display: none;
  }
}
.details {
  background-color: #c5fcee;
  opacity: 0;
  border: 5px solid black;
}
.link{
  display: none;
}
.v-application .head {
  width: 27vw;
   background-image: linear-gradient(to right top, #4e4e4e, #545357, #585960, #5d5f6a, #606574, #657286, #688098, #688eaa, #63a8c5, #59c4db, #54e0ea, #5ffbf1);
  border: 5px solid black;
  justify-content: center;
  border-bottom: 0px;
  padding-top: 4px;
  margin: 0px;
}
.summ{
  display: none;
  background-color: #85123f;
  padding:2px;
  border-radius: 7%;
}
.v-application .foot {
  width: 27vw;
   background-image: linear-gradient(to right top, #4e4e4e, #545357, #585960, #5d5f6a, #606574, #657286, #688098, #688eaa, #63a8c5, #59c4db, #54e0ea, #5ffbf1);
  border: 5px solid black;
  justify-content: center;
  border-top: 0px;
  padding-top: 4px;
  padding-bottom: 4px;
  margin: 0px;
}

</style>
