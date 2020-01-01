<template>
  <div class='projectcard'>
    <p class='headline font-weight-bold text-uppercase text-center'>{{ project.name}}</p><br>
    <p class='subtitle-2 te'>{{ project.summary }}</p>
    <p class='body-2 font-weight-light'><a :href="`${ project.link }`">{{ project.link }}</a></p>
    <p class='body-2 font-weight-light'><a :href="`${ project.github }`">{{ project.github }}</a></p>
  </div>
</template>

<script>
export default {
  props: [ 'project' ]
}
</script>
<style lang='scss'>
.projectcard {
    background-color: aliceblue;
    padding: 2vw;
    padding-top: 3vw;
    width: 32vw;
    height: 21vw;
    margin:5vw;
    border: 10px solid black;
}
.projectcard:hover{
    background-image: url('../assets/SNS.jpg');
    background-attachment: fixed;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    transition: all 1s easy 0s;
}
</style>
