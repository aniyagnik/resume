<template>
  <div class="box">
      <p style='font-size: 1.5em' class='head font-weight-bold text-uppercase text-center'>{{ project.name}}</p>
    <div class='projectcard'>
      <!-- :style="`background-image:url(${project.image})`" -->
      <div class='image' ></div>
      <div class='details text-center'>
        <p style='font-size: 1.1em' class='summ font-weight-black white--text'>{{ project.summary }}</p>
        <p style='font-size: 1em' class='link font-weight-light'>
          <kbd>github link</kbd>&nbsp;
          <code><a :href="`${ project.github }`">{{ project.github }}</a></code>
        </p>
      </div>
    </div>
    <p style='font-size: 1em' class='foot font-weight-light text-center'>
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
  background-image: url('../assets/quiz.jpg');
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
  overflow: auto;
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

@media only screen and (max-width: 1050px) {
 .projectcard {
    width: 40vw;
    height: 32vw;
  }
  .image{
    width: 40vw;
    height: 32vw;
  }
  .projectcard:hover{
    .details{
      width: 40vw;
      height: 32vw;
    }
  }
  .v-application .head {
    width: 40vw;
  }
  .v-application .foot {
    width: 40vw;
  }
}
@media only screen and (max-width: 850px) {
 .projectcard {
    width: 45vw;
    height: 32vw;
  }
  .head{
    font-size: 1.3em;
  }
  .image{
    width: 45vw;
    height: 32vw;
  }
  .projectcard:hover{
    .details{
      width: 45vw;
      height: 32vw;
    }
  }
  .v-application .head {
    width: 45vw;
  }
  .v-application .foot {
    width: 45vw;
  }
}

@media only screen and (max-width: 668px) {
 .projectcard {
    width: 70vw;
    height: 50vw;
  }
  .image{
    width: 70vw;
    height: 50vw;
  }
  .projectcard:hover{
    .details{
      width: 70vw;
      height: 50vw;
    }
  }
  .v-application .head {
    width: 70vw;
  }
  .v-application .foot {
    width: 70vw;
  }
}

@media only screen and (max-width: 438px) {
 .projectcard {
    width: 94vw;
    height: 70vw;
  }
  .image{
    width: 94vw;
    height: 70vw;
  }
  .projectcard:hover{
    .details{
      width: 94vw;
      height: 70vw;
    }
  }
  .v-application .head {
    width: 94vw;
  }
  .v-application .foot {
    width: 94vw;
  }
}
</style>
